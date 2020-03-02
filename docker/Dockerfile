FROM envoyproxy/envoy-build-centos:b6c2bae5716a289fd68c45a6e5bc16979dbe69c5

COPY ./envoy/ /source

RUN groupadd --gid $(id -g) -f envoygroup

RUN useradd -o --uid $(id -u) --gid $(id -g) --no-create-home --home-dir /source envoybuild

RUN usermod -a -G pcap envoybuild

USER envoybuild

ENTRYPOINT ["tail", "-f", "/dev/null"]
