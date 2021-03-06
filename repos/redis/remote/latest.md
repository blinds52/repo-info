## `redis:latest`

```console
$ docker pull redis@sha256:3446883dfe13ab3db67433aace0e72d8cd669c528e60c617c42d6c697f0fa41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:latest` - linux; amd64

```console
$ docker pull redis@sha256:0d9e5a4a3072948e1460a510bb07b2636d5c160ee84edb98daac8e779756f08d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39394938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861cc310cd916417a1f84c0293c5ce3ea24c0c8d4c0e7a845cb6988ecf5a3241`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:34 GMT
ADD file:e7ac45803c3ab9b7023933b75f5a88eda1f3edca97c7e462401860777cf312f7 in / 
# Tue, 12 Dec 2017 01:41:35 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:11:57 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Tue, 12 Dec 2017 07:11:57 GMT
ENV GOSU_VERSION=1.10
# Tue, 12 Dec 2017 07:12:20 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Wed, 24 Jan 2018 22:32:58 GMT
ENV REDIS_VERSION=4.0.7
# Wed, 24 Jan 2018 22:32:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.7.tar.gz
# Wed, 24 Jan 2018 22:32:59 GMT
ENV REDIS_DOWNLOAD_SHA=1bba546d44fb40e1fd8be1a15e1a9cc6484bceeea0bbd52919eebc656661ecd1
# Wed, 24 Jan 2018 22:33:46 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Jan 2018 22:33:47 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 22:33:47 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 22:33:48 GMT
WORKDIR /data
# Wed, 24 Jan 2018 22:33:48 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Wed, 24 Jan 2018 22:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 22:33:48 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 22:33:49 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c4bb02b17bb4b034c95a948c99c762cf0486a45f45441a052208d7750f1b413b`  
		Last Modified: Tue, 12 Dec 2017 01:48:52 GMT  
		Size: 30.1 MB (30114519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58638acf67c5d1d65732b562d5a7f5525b9788155cc10d4cd96c3d5380fadf04`  
		Last Modified: Tue, 12 Dec 2017 07:17:40 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98d108cc38bde856021760374435ab87fa2ef7c4317cd18fd7b7ded7af506a3`  
		Last Modified: Tue, 12 Dec 2017 07:17:40 GMT  
		Size: 981.7 KB (981699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cde9c78d521b0461273f888b2ad76a01ee76440378107a92d786d8a5576f06`  
		Last Modified: Wed, 24 Jan 2018 22:36:33 GMT  
		Size: 8.3 MB (8296132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f171693d37f9483291043024064f09fa6d0d8390e04553f8585c5e71a518ebf2`  
		Last Modified: Wed, 24 Jan 2018 22:36:32 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48076ff6ff36c7cb4e1c75a16c91441fbaed46b9cce7b9afb66d4df1d06459f`  
		Last Modified: Wed, 24 Jan 2018 22:36:32 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; arm variant v5

```console
$ docker pull redis@sha256:1f3cd78fec7178b2e32dcac6f0874a17028c2935389767b0747e220800e10686
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37590785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d9bf78c8425c28543122bbd2c1e12c425904711495904064ba553ccef85536`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Dec 2017 20:57:33 GMT
ADD file:29d0e44ebcc6f8dc2cfbc86c5034380677d263e9eec27a22ba045e0810836f81 in / 
# Tue, 12 Dec 2017 20:57:34 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 23:14:35 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Tue, 12 Dec 2017 23:14:35 GMT
ENV GOSU_VERSION=1.10
# Tue, 12 Dec 2017 23:15:21 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 25 Jan 2018 15:09:38 GMT
ENV REDIS_VERSION=4.0.7
# Thu, 25 Jan 2018 15:09:38 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.7.tar.gz
# Thu, 25 Jan 2018 15:09:38 GMT
ENV REDIS_DOWNLOAD_SHA=1bba546d44fb40e1fd8be1a15e1a9cc6484bceeea0bbd52919eebc656661ecd1
# Thu, 25 Jan 2018 15:10:45 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 25 Jan 2018 15:10:46 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 25 Jan 2018 15:10:46 GMT
VOLUME [/data]
# Thu, 25 Jan 2018 15:10:46 GMT
WORKDIR /data
# Thu, 25 Jan 2018 15:10:46 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 25 Jan 2018 15:10:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2018 15:10:47 GMT
EXPOSE 6379/tcp
# Thu, 25 Jan 2018 15:10:47 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:51e696f556166d0e25b3b27c824c4aafbddd5adcfd3f5186c09707f7baa3b312`  
		Last Modified: Tue, 12 Dec 2017 21:07:41 GMT  
		Size: 28.4 MB (28423526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0206b9cb3a70c21180f01a2532fe2c5a436a48e5fc5d8b939ba69b7d61c80a3a`  
		Last Modified: Tue, 12 Dec 2017 23:18:09 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f18f2f5d7b2619f7683612c23f23c54c1f09a9ac9f5714f36e1ff47dffac347`  
		Last Modified: Tue, 12 Dec 2017 23:18:13 GMT  
		Size: 971.2 KB (971228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc77eb4ac2bcb3006e542d79c6094071833b0c309d7989e3bae3e121e7317c13`  
		Last Modified: Thu, 25 Jan 2018 15:11:05 GMT  
		Size: 8.2 MB (8193419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c18a0592ab6b73a24179185c5cbb01ad0ff46d0524517fe25b5909a06f6c41`  
		Last Modified: Thu, 25 Jan 2018 15:11:04 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dda4ab8c35fe9bfd1ebaec8ba5af567178cac5c0801e9bbdcad5d4008816d9`  
		Last Modified: Thu, 25 Jan 2018 15:11:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; arm variant v7

```console
$ docker pull redis@sha256:5f0cc2c8536f640a27aac4cc904421d33c5733d7500bc75212d88e0e1d9b9420
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35175338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516bccaaabad54b490a035d94dec795d90bfa618e3e33e062aff1aa58913993e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Dec 2017 13:27:47 GMT
ADD file:1f5de474caa19da14d698a3f9c3d161abfa1e19e258a596d64f3dfc9e2f17686 in / 
# Tue, 12 Dec 2017 13:27:47 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 16:40:56 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Tue, 12 Dec 2017 16:40:56 GMT
ENV GOSU_VERSION=1.10
# Tue, 12 Dec 2017 16:41:50 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 25 Jan 2018 01:27:35 GMT
ENV REDIS_VERSION=4.0.7
# Thu, 25 Jan 2018 01:27:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.7.tar.gz
# Thu, 25 Jan 2018 01:27:35 GMT
ENV REDIS_DOWNLOAD_SHA=1bba546d44fb40e1fd8be1a15e1a9cc6484bceeea0bbd52919eebc656661ecd1
# Thu, 25 Jan 2018 01:28:33 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 25 Jan 2018 01:28:34 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 25 Jan 2018 01:28:34 GMT
VOLUME [/data]
# Thu, 25 Jan 2018 01:28:34 GMT
WORKDIR /data
# Thu, 25 Jan 2018 01:28:34 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 25 Jan 2018 01:28:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2018 01:28:35 GMT
EXPOSE 6379/tcp
# Thu, 25 Jan 2018 01:28:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4b9c0f1a415433a98643bdda391dcf4fe5d9653fc3ed3845c7ac1be99eb43399`  
		Last Modified: Tue, 12 Dec 2017 13:39:52 GMT  
		Size: 26.3 MB (26282714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6835fe576543df3c87405f33db99aa1f040e3f241c5e5d72ffb416953902b8`  
		Last Modified: Tue, 12 Dec 2017 16:44:59 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11c10ad12017478481b1755839ece7c69945ee8c04b97bb10909db85e4ed338`  
		Last Modified: Tue, 12 Dec 2017 16:44:59 GMT  
		Size: 956.1 KB (956126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643319e3b71415a5430d16d070f9d6dff68c5de4d530802e74cdb62e7d057abe`  
		Last Modified: Thu, 25 Jan 2018 01:29:02 GMT  
		Size: 7.9 MB (7933884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e472c51cc372b46dd199390772dc2b1ffe87c0cf8880be7312b69bf0b26dc0`  
		Last Modified: Thu, 25 Jan 2018 01:28:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f864ec9fcc5981185cf8aa452f762a43bc1ea82fd0bad4418494c9bd87b896`  
		Last Modified: Thu, 25 Jan 2018 01:28:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:e14a70b8ce66d4cbcd55aced3d9d0f1471fcf807e889ba5b5ddcf4a065bc0bd9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0c61c9b8508a9a664e04cea650414d4836cc1057d71ce8b4df0ce7811fb356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Dec 2017 18:26:03 GMT
ADD file:da6be268a98d89a43438155746ca6d08f474e9aa85c64699f50445352b46c348 in / 
# Tue, 12 Dec 2017 18:26:04 GMT
CMD ["bash"]
# Wed, 20 Dec 2017 13:25:39 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Wed, 20 Dec 2017 13:25:40 GMT
ENV GOSU_VERSION=1.10
# Wed, 20 Dec 2017 13:26:36 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 25 Jan 2018 13:25:50 GMT
ENV REDIS_VERSION=4.0.7
# Thu, 25 Jan 2018 13:25:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.7.tar.gz
# Thu, 25 Jan 2018 13:25:52 GMT
ENV REDIS_DOWNLOAD_SHA=1bba546d44fb40e1fd8be1a15e1a9cc6484bceeea0bbd52919eebc656661ecd1
# Thu, 25 Jan 2018 13:27:38 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 25 Jan 2018 13:27:40 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 25 Jan 2018 13:27:40 GMT
VOLUME [/data]
# Thu, 25 Jan 2018 13:27:41 GMT
WORKDIR /data
# Thu, 25 Jan 2018 13:27:41 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 25 Jan 2018 13:27:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2018 13:27:43 GMT
EXPOSE 6379/tcp
# Thu, 25 Jan 2018 13:27:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8e9df51286bbe86a4cb3ffe54327681ab34b9b6d62c3f4e187ffc677125e4780`  
		Last Modified: Tue, 12 Dec 2017 18:41:37 GMT  
		Size: 27.5 MB (27480582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075c247daad6bb45a002c0a24377355e91aef8e96dbc920ef85b5f95dba5d597`  
		Last Modified: Wed, 20 Dec 2017 13:31:04 GMT  
		Size: 2.1 KB (2100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671b4ef947e36f312884f8d49f560e5191e57a0e583820b56b530e7ff03d771f`  
		Last Modified: Wed, 20 Dec 2017 13:31:04 GMT  
		Size: 948.7 KB (948652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb32f805e1d0b1e25927bd1f1508a3e8e48c6b6aafbd1c506e27c52958895f8`  
		Last Modified: Thu, 25 Jan 2018 13:29:58 GMT  
		Size: 8.4 MB (8441951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cc91426e9de934ee94336eac7900d7c246eeaf91ce1194585a9c878a2de47d`  
		Last Modified: Thu, 25 Jan 2018 13:29:52 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13e7ced4bebe6fbd1148e760eccf8c78009e872dd2408591cbc9becbd0ef5ee`  
		Last Modified: Thu, 25 Jan 2018 13:29:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; 386

```console
$ docker pull redis@sha256:1dd9efbd6a981cbb832266357b75238cd1435e6833b9cce4b18f4843d0d80dfb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38740267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9caad80c4f13153d9ad721b052fab7aa9d83e3f19f223fef09c8e739d8bf4657`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Dec 2017 14:21:05 GMT
ADD file:d31765999b40e32b628f3ec72b762f007f4918b08c507484e425adc990c87c26 in / 
# Tue, 12 Dec 2017 14:21:05 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 21:03:38 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Tue, 12 Dec 2017 21:03:38 GMT
ENV GOSU_VERSION=1.10
# Tue, 12 Dec 2017 21:04:16 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 25 Jan 2018 14:45:50 GMT
ENV REDIS_VERSION=4.0.7
# Thu, 25 Jan 2018 14:45:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.7.tar.gz
# Thu, 25 Jan 2018 14:45:50 GMT
ENV REDIS_DOWNLOAD_SHA=1bba546d44fb40e1fd8be1a15e1a9cc6484bceeea0bbd52919eebc656661ecd1
# Thu, 25 Jan 2018 14:47:03 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 25 Jan 2018 14:57:11 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 25 Jan 2018 14:57:12 GMT
VOLUME [/data]
# Thu, 25 Jan 2018 14:57:12 GMT
WORKDIR /data
# Thu, 25 Jan 2018 14:57:12 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 25 Jan 2018 14:57:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2018 14:57:13 GMT
EXPOSE 6379/tcp
# Thu, 25 Jan 2018 14:57:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6b323e7c684c46ec9e577d3acb692c7e1c0c26ffbea6a4530dbe784a7eedf0f7`  
		Last Modified: Tue, 12 Dec 2017 14:49:35 GMT  
		Size: 30.3 MB (30266257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b36a22b0f548b632d8bc28aa752a7c776351e3fa3c167b13901a9a648dff0f`  
		Last Modified: Tue, 12 Dec 2017 21:11:34 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625bd220ae9238fdcd1a3e9db810236dc47502995b93d54b4a7bc5f474508112`  
		Last Modified: Tue, 12 Dec 2017 21:11:34 GMT  
		Size: 960.8 KB (960808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7151ffc3f2f2b72256a6495c0312dbe04fca7ffea2814f22dff663be2431bf72`  
		Last Modified: Thu, 25 Jan 2018 15:23:12 GMT  
		Size: 7.5 MB (7510625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2134e052b431766f88f05130b4c7c5c28408edfee729214e9643b019549c8418`  
		Last Modified: Thu, 25 Jan 2018 15:23:09 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52275db2f67c8fcf0b3474099de9e674013f7a87226a7b001ef3ea1734235f44`  
		Last Modified: Thu, 25 Jan 2018 15:23:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; ppc64le

```console
$ docker pull redis@sha256:3270ac4c5bba5572987eed0d39936a9d8cbe6b01137043b731b7a95b0057003c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38915938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6710758a4e63b7802dc7071b54d6a03deea78bd9cf0120a4c140f832d0563d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Dec 2017 01:33:17 GMT
ADD file:db3712029b01ae02058b528d156cfdf714f7f2b5fc30216a349f13c15ff9fd67 in / 
# Tue, 12 Dec 2017 01:33:18 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 06:40:30 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Tue, 12 Dec 2017 06:40:32 GMT
ENV GOSU_VERSION=1.10
# Tue, 12 Dec 2017 06:42:22 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 25 Jan 2018 06:35:24 GMT
ENV REDIS_VERSION=4.0.7
# Thu, 25 Jan 2018 06:35:25 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.7.tar.gz
# Thu, 25 Jan 2018 06:35:27 GMT
ENV REDIS_DOWNLOAD_SHA=1bba546d44fb40e1fd8be1a15e1a9cc6484bceeea0bbd52919eebc656661ecd1
# Thu, 25 Jan 2018 06:37:36 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 25 Jan 2018 06:37:40 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 25 Jan 2018 06:37:41 GMT
VOLUME [/data]
# Thu, 25 Jan 2018 06:37:43 GMT
WORKDIR /data
# Thu, 25 Jan 2018 06:37:44 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 25 Jan 2018 06:37:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2018 06:37:47 GMT
EXPOSE 6379/tcp
# Thu, 25 Jan 2018 06:37:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f90148bfa218fdcac96e1ad5dd98070db3f45afdca6148d5d71bb9c4b12e5776`  
		Last Modified: Tue, 12 Dec 2017 01:39:02 GMT  
		Size: 29.3 MB (29306117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f662385d2726c68cbb1dde138126e2577b69f2f75edb031782b33056fcca8e15`  
		Last Modified: Tue, 12 Dec 2017 06:50:31 GMT  
		Size: 2.1 KB (2098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d4e7f0b93f593fb94ad43d33ba101f2f418b2ce017189138ab2b434f5a6b19`  
		Last Modified: Tue, 12 Dec 2017 06:50:31 GMT  
		Size: 950.7 KB (950658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcd6a3c11211a5f560b59250afc9d3365eb9b2a3ee55f3616e61481950d9fe6`  
		Last Modified: Thu, 25 Jan 2018 06:39:18 GMT  
		Size: 8.7 MB (8656530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277a97402b140f8be118793f62cbf3c54241e5eabce65a2de8cd06ec8d463919`  
		Last Modified: Thu, 25 Jan 2018 06:39:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690071c0c2442b020a0fd974020a7142596db33502bdc5ca4e1dadd5278e60a3`  
		Last Modified: Thu, 25 Jan 2018 06:39:15 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; s390x

```console
$ docker pull redis@sha256:b6724918b313d9572099e7742f421ab7cc3d8da2692bb53d9f9af417252cbacc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40195712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc1f18ed9a6a12348c80e717b312d867f89113c2db7f9292bc0e9f121ce23bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Dec 2017 06:23:05 GMT
ADD file:68877912183dff16971679b6264399a76d678986d7cf02bbba2e006d91077cf3 in / 
# Tue, 12 Dec 2017 06:23:06 GMT
CMD ["bash"]
# Sun, 07 Jan 2018 09:26:06 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Sun, 07 Jan 2018 09:26:06 GMT
ENV GOSU_VERSION=1.10
# Sun, 07 Jan 2018 09:26:33 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 25 Jan 2018 06:24:34 GMT
ENV REDIS_VERSION=4.0.7
# Thu, 25 Jan 2018 06:24:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.7.tar.gz
# Thu, 25 Jan 2018 06:24:34 GMT
ENV REDIS_DOWNLOAD_SHA=1bba546d44fb40e1fd8be1a15e1a9cc6484bceeea0bbd52919eebc656661ecd1
# Thu, 25 Jan 2018 06:25:09 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 25 Jan 2018 06:25:09 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 25 Jan 2018 06:25:09 GMT
VOLUME [/data]
# Thu, 25 Jan 2018 06:25:09 GMT
WORKDIR /data
# Thu, 25 Jan 2018 06:25:10 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 25 Jan 2018 06:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2018 06:25:10 GMT
EXPOSE 6379/tcp
# Thu, 25 Jan 2018 06:25:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7ef9b5c13de473137c3ae16d379a5f152b59921d4e96887c06f9e1291af84691`  
		Last Modified: Thu, 14 Dec 2017 00:53:34 GMT  
		Size: 30.3 MB (30293639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608e779e09f2eff9338668b6f32d30ad6db5824db6e05a40163baa53af8a4732`  
		Last Modified: Sun, 07 Jan 2018 09:28:52 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3bc2bf99d2d3b8b7af50eabf05bcd385693d216437119560e8b76a250123d1`  
		Last Modified: Sun, 07 Jan 2018 09:28:52 GMT  
		Size: 966.9 KB (966920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe6690836025a6cd02870ce6ccc0fe3a49f1ba82efc81fc60f36e741c1c729d`  
		Last Modified: Thu, 25 Jan 2018 06:25:51 GMT  
		Size: 8.9 MB (8932557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759ea79d77c7d5960725ec2933bd6b5472b9ec749e2f262badd72d5142311d2f`  
		Last Modified: Thu, 25 Jan 2018 06:25:49 GMT  
		Size: 97.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c35db18ae3b6e944ebb9a2af5a324c6b98eed51da07064412212c1b2589db9`  
		Last Modified: Thu, 25 Jan 2018 06:25:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
