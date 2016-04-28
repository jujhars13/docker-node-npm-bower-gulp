# docker-node-npm-bower-gulp
Node.js w/ NPm and Bower &amp; Grunt for automated builds and deployments where you want to fix the node version.

Inspired by [DigitallySeamless/docker-nodejs-bower-grunt](https://github.com/DigitallySeamless/docker-nodejs-bower-grunt/)

[![dockeri.co](http://dockeri.co/image/jujhars13/docker-node-npm-bower-gulp)](https://hub.docker.com/r/jujhars13/docker-node-npm-bower-gulp/)


### Usage
Your project should be mapped to the `/data` directory as that's the default eg

    docker run -it --rm -v ${PWD}:/data jujhars13/docker-node-npm-bower-gulp

#### Run `node`

    docker run -it --rm jujhars13/docker-node-npm-bower-gulp node

#### Run `npm`

    docker run -it --rm jujhars13/docker-node-npm-bower-gulp npm

#### Run `bower`

    docker run -it --rm jujhars13/docker-node-npm-bower-gulp bower

#### Run `gulp`

    docker run -it --rm jujhars13/docker-node-npm-bower-gulp gulp

## Supported Tags
Relating to the major nodejs version.

- [4](https://github.com/jujhars13/docker-node-npm-bower-gulp/blob/4/Dockerfile)
- [5](https://github.com/jujhars13/docker-node-npm-bower-gulp/blob/5/Dockerfile)
- [latest](https://github.com/jujhars13/docker-node-npm-bower-gulp/blob/master/Dockerfile)

### Usage
So if you want to use Node V4

    docker run -it --rm -v ${PWD}:/data jujhars13/docker-node-npm-bower-gulp:4
