## `mongo:latest`

```console
$ docker pull mongo@sha256:878b76e5834f37da98096296f4147f6ca4d94b1a9187986e9d6e59756e7ce865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:8bb68343e860575cfe3e82c98f5f5baad3ab8a67f54062d3476f2276b576abb4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130406419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f57644645eb53a3d2256f460ade116ad3590252c28f63e5136c026423dc8286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:34 GMT
ADD file:e7ac45803c3ab9b7023933b75f5a88eda1f3edca97c7e462401860777cf312f7 in / 
# Tue, 12 Dec 2017 01:41:35 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 02:36:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 12 Dec 2017 02:38:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2017 01:16:42 GMT
ENV GOSU_VERSION=1.10
# Thu, 21 Dec 2017 01:16:42 GMT
ENV JSYAML_VERSION=3.10.0
# Thu, 21 Dec 2017 01:17:01 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-get purge -y --auto-remove wget
# Thu, 21 Dec 2017 01:17:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 21 Dec 2017 01:21:07 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Thu, 21 Dec 2017 01:21:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 21 Dec 2017 01:21:17 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 21 Dec 2017 01:21:18 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 21 Dec 2017 01:21:18 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 21 Dec 2017 01:21:18 GMT
ENV MONGO_MAJOR=3.6
# Mon, 15 Jan 2018 23:15:02 GMT
ENV MONGO_VERSION=3.6.2
# Mon, 15 Jan 2018 23:15:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 15 Jan 2018 23:15:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 15 Jan 2018 23:15:25 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 15 Jan 2018 23:15:25 GMT
VOLUME [/data/db /data/configdb]
# Mon, 15 Jan 2018 23:15:25 GMT
COPY file:18c5d9b642a89adf49e037d95a9e7de6b60557c77e049c9652605cf9cba57df9 in /usr/local/bin/ 
# Mon, 15 Jan 2018 23:15:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 Jan 2018 23:15:26 GMT
EXPOSE 27017/tcp
# Mon, 15 Jan 2018 23:15:26 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c4bb02b17bb4b034c95a948c99c762cf0486a45f45441a052208d7750f1b413b`  
		Last Modified: Tue, 12 Dec 2017 01:48:52 GMT  
		Size: 30.1 MB (30114519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f58e3bb3be4bfc57e890138990e250f521d69af3a0c39c7d0394727c66dc676`  
		Last Modified: Tue, 12 Dec 2017 02:41:52 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a229fb575a6e558f699a74bc9037d818b6d74c607e68ef6cf1c548daf10ebc52`  
		Last Modified: Tue, 12 Dec 2017 02:42:30 GMT  
		Size: 2.4 MB (2397783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5ddc533743964c2e280d7a7e70667e892c29b518c04ee34aa56aa9449b59da`  
		Last Modified: Thu, 21 Dec 2017 01:23:21 GMT  
		Size: 816.7 KB (816688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9d2af6e2069f3050614a5f983f7147427a7f4e907c67bbb070e346ab333ed5`  
		Last Modified: Thu, 21 Dec 2017 01:23:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6c28c0235b619029c8b8c9d512f97756a986bfa458e64b5aa45784af894ac3`  
		Last Modified: Thu, 21 Dec 2017 01:24:43 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6688308f715efc799218462de2504d5ea35be542dfc7bb1dbcbf9298f4c055d`  
		Last Modified: Mon, 15 Jan 2018 23:25:37 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07c56202c1a956ce919db56d3e09890a3df459cefab949e517810b84e6c2378`  
		Last Modified: Mon, 15 Jan 2018 23:26:02 GMT  
		Size: 97.1 MB (97069699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd9b5a8a42871d8a15d6dd892cb7947fa345445ded44f610117ec4cbbe7bf81`  
		Last Modified: Mon, 15 Jan 2018 23:25:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf24480e18299ebb064cdaa4947195f9996a9b443f3c44dcc9cc1dbe668b82e`  
		Last Modified: Mon, 15 Jan 2018 23:25:37 GMT  
		Size: 3.7 KB (3718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
