# K8S-MICRO-SSR-COMMON

### Docker Image

```sh
docker build -t k8s-micro-ssr-common:1.0.0 .  --no-cache
docker tag k8s-micro-ssr-common:1.0.0 hackerlinner/k8s-micro-ssr-common:1.0.0

docker run -it -p 3000:3000 hackerlinner/k8s-micro-ssr-common:1.0.0

docker run -p 3000:3000 -it hackerlinner/k8s-micro-ssr-common:1.0.0 /bin/sh -c "
env SSR_HOME_TARGET='http://172.28.15.236:3001'  \
env SSR_ABOUT_TARGET='http://172.28.15.236:3002'  \
yarn start"
```