# AUTOGENERATED FILE
FROM resin/armhf-debian:jessie

ENV NODE_VERSION 8.6.0

RUN buildDeps='curl' \
	&& set -x \
	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends \
	&& rm -rf /var/lib/apt/lists/* \
	&& curl -SLO "http://resin-packages.s3.amazonaws.com/node/v$NODE_VERSION/node-v$NODE_VERSION-linux-alpine-armhf.tar.gz" \
	&& echo "cdde50f85efd710634a8f8216d87da7473456d2e8587d68af516ac4ea16a5cc0  node-v8.6.0-linux-alpine-armhf.tar.gz" | sha256sum -c - \
	&& tar -xzf "node-v$NODE_VERSION-linux-alpine-armhf.tar.gz" -C /usr/local --strip-components=1 \
	&& rm "node-v$NODE_VERSION-linux-alpine-armhf.tar.gz" \
	&& apt-get purge -y --auto-remove $buildDeps \
	&& npm config set unsafe-perm true -g --unsafe-perm \
	&& rm -rf /tmp/*

CMD ["echo","'No CMD command was set in Dockerfile! Details about CMD command could be found in Dockerfile Guide section in our Docs. Here's the link: http://docs.resin.io/deployment/dockerfile"]
