FROM envoyproxy/envoy-build-centos:83ce22dd47a73b4f03f6787b089e11f758c83484

COPY ./envoy/ /source

RUN groupadd --gid $(id -g) -f envoygroup

RUN useradd -o --uid $(id -u) --gid $(id -g) --no-create-home --home-dir /source envoybuild

RUN usermod -a -G pcap envoybuild

USER envoybuild

ENTRYPOINT ["tail", "-f", "/dev/null"]
~                                                  
