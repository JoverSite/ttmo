FROM node
MAINTAINER Jover Zhang <joverzh@gmail.com>

# npm registry image accelerate
ARG NPM_REGISTRY

# code repo
ARG FRONT_REPO
ARG BACK_REPO

# git branch
ARG FRONT_BRANCH
ARG BACK_BRANCH

RUN git clone -b $BACK_BRANCH $BACK_REPO project && \
    cd project && \
    yarn install --registry $NPM_REGISTRY && \
    cd / && \
    git clone -b $FRONT_BRANCH $FRONT_REPO package && \
    mv /package/dist/js /project/src/static/js && \
    mv /package/dist/css /project/src/static/css && \
    mv /package/dist/index.html /project/src/static/index.html

WORKDIR /project

ENTRYPOINT ["yarn", "run", "start"]
CMD ["--port", "8080"]
