# MICRO-SSR-COMMON

### Docker Image

```sh
docker build -t micro-ssr-common:1.0.0 .  --no-cache
docker tag micro-ssr-common:1.0.0 hackerlinner/micro-ssr-common:1.0.0

docker run -it -p 3000:3000 hackerlinner/micro-ssr-common:1.0.0

docker run -p 3000:3000 -it hackerlinner/micro-ssr-common:1.0.0 /bin/sh -c "
env SSR_HOME_TARGET='http://172.28.15.236:3001'  \
env SSR_ABOUT_TARGET='http://172.28.15.236:3002'  \
yarn start"
```