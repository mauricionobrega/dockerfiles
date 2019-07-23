# CREATE IMAGE:
```
  docker build -t [DOCKERHUB_USERNAME]/node:10.16.0-alpine .
```

# RUN IMAGE:
```
  docker run -it [DOCKERHUB_USERNAME]/node:10.16.0-alpine /bin/bash
```

# DOCKERFILE SAMPLE
```
FROM mauricionobrega/node:10.16.0-alpine


# ... REST OF DOCKERFILE
```
