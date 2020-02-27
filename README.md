# docker
```shell
docker build -t xpanda/envoy-build-centos:v1.13.0 .
```

# container
```shell
git clone https://github.com/envoyproxy/envoy.git
git checkout v1.13.0
git branch -a
./ci/run_envoy_docker.sh
./ci/do_ci.sh bazel.release
```
