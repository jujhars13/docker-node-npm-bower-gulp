# docker-node-npm-bower-gulp
Node.js w/ NPM, Bower and Grunt for automated builds and deployments where you want to fix the node version.  Node V6 broke our automated builds and so we needed this repo.

We're using this image at [Voxpopme](https://www.voxpopme.com) to ensure we have consistent builds of our angular apps.

Inspired by [DigitallySeamless/docker-nodejs-bower-grunt](https://github.com/DigitallySeamless/docker-nodejs-bower-grunt/)

[![dockeri.co](http://dockeri.co/image/jujhars13/docker-node-npm-bower-gulp)](https://hub.docker.com/r/jujhars13/docker-node-npm-bower-gulp/)


### Usage
Your project directory should be mapped to the `/data` directory:

    docker run -it --rm -v ${PWD}:/data jujhars13/docker-node-npm-bower-gulp <cmd>

#### Run `node`

    docker run -ti --rm -v ${PWD}:/data jujhars13/docker-node-npm-bower-gulp node

#### Run `npm install`

    docker run --rm -v ${PWD}:/data jujhars13/docker-node-npm-bower-gulp npm install

#### Run `bower install `

    docker run --rm -v ${PWD}:/data jujhars13/docker-node-npm-bower-gulp bower install

#### Run `gulp build`
**NB** the `DISABLE_NOTIFIER=true` env var that's passed in as gulp-notify doesn't play well if the terminal is not attached [@see](https://github.com/mikaelbr/gulp-notify)

```
    docker run \
    --rm -v ${PWD}:/data \
    -e DISABLE_NOTIFIER=true \
    jujhars13/docker-node-npm-bower-gulp \
    gulp build
```

## Supported Tags
Relating to the major nodejs version.

- [4](https://github.com/jujhars13/docker-node-npm-bower-gulp/blob/4/Dockerfile)
- [5](https://github.com/jujhars13/docker-node-npm-bower-gulp/blob/5/Dockerfile)
- [latest](https://github.com/jujhars13/docker-node-npm-bower-gulp/blob/master/Dockerfile)

### Usage
So if you want to use Node V4

    docker run --rm -v ${PWD}:/data jujhars13/docker-node-npm-bower-gulp:4 bower install
