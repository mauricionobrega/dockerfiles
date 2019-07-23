FROM node:10.16.0-alpine

# INFO
MAINTAINER Mauricio Nobrega <mauricio.nobrega@gmail.com>
LABEL maintainer='mauricio.nobrega@gmail.com'
LABEL built_in='[alpine@3.9.4, nodejs@10.16.0, yarn@1.17.3, nvm@0.34.0]'
LABEL site='https://hub.docker.com/u/mauricionobrega/content'
LABEL build_date='2019-07-23'

# UPDATE ALPINE
RUN apk update
RUN apk add -U curl bash ca-certificates openssl ncurses coreutils python2 make gcc g++ libgcc linux-headers grep util-linux binutils findutils

# PREPARE
RUN export NODE_VERSION=10.16.0
ENV NODE_VERSION=$NODE_VERSION
RUN touch ~/.bashrc

# INSTALL YARN
RUN curl -o- -L https://yarnpkg.com/install.sh | bash -s -- --version 1.17.3

# INSTALL NVM
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
RUN npm config delete prefix
RUN echo 'export NVM_DIR="$HOME/.nvm" && [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"' > $HOME/.bashrc

# PREPARE NVM
RUN chmod +x $HOME/.bashrc
RUN cat $HOME/.bashrc
RUN source $HOME/.bashrc
RUN . $HOME/.nvm/nvm.sh
