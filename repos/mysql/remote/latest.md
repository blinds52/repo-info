## `mysql:latest`

```console
$ docker pull mysql@sha256:7cdb08f30a54d109ddded59525937592cb6852ff635a546626a8960d9ec34c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:83204528ade605ce7ff02bead28378f7055e91d4c73f18e099dcf3126dbb240a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144377812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f008d8ff927dc527c5a57251b45cead7c9259c16a6a93c144f397eaafc103d36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 02:17:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Dec 2017 02:22:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 12 Dec 2017 02:23:10 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 12 Dec 2017 02:23:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Dec 2017 02:23:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 02:23:23 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Dec 2017 02:23:52 GMT
ENV MYSQL_MAJOR=5.7
# Mon, 15 Jan 2018 21:45:44 GMT
ENV MYSQL_VERSION=5.7.21-1debian8
# Mon, 15 Jan 2018 21:45:45 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Mon, 15 Jan 2018 21:46:12 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Mon, 15 Jan 2018 21:46:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 15 Jan 2018 21:46:12 GMT
COPY file:52f06a5715711e8cca267af294ae8a41bd51b2c2ba4c9dd66ee8f53c6fc96dae in /usr/local/bin/ 
# Mon, 15 Jan 2018 21:46:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 Jan 2018 21:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 Jan 2018 21:46:14 GMT
EXPOSE 3306/tcp
# Mon, 15 Jan 2018 21:46:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78032de49d65ab1151d278821068401fa7a8964c16b2f4441a3ef9ac8dd02229`  
		Last Modified: Tue, 12 Dec 2017 02:23:47 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837546b20bc4af04c4cd0b34ac6cb74418f0400fa80045d02d341aecbc70f928`  
		Last Modified: Tue, 12 Dec 2017 02:34:38 GMT  
		Size: 1.3 MB (1303017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8316af6cc601a268bccfd58f93c2598e4a5f8a6b101cb9ffe365bcd467cb8e`  
		Last Modified: Tue, 12 Dec 2017 02:34:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1056cf29b9f156636008257f45baf554adb9e1587e3eab7eaf07fda577e75ffa`  
		Last Modified: Tue, 12 Dec 2017 02:34:38 GMT  
		Size: 10.7 MB (10711163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f3913b029a07790d452d2812d9d340cff1668930d6c69a5f3ee6cd63edbe97`  
		Last Modified: Tue, 12 Dec 2017 02:34:34 GMT  
		Size: 20.1 KB (20149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98eea8321cafaa989e480400135a48855fe2f17fbf88b16f21adf6b132017af`  
		Last Modified: Mon, 15 Jan 2018 22:17:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8e3ebdeaf554387932484bf93f67f26d4bbb20d76eeb231b9b694efbf6a2ee`  
		Last Modified: Mon, 15 Jan 2018 22:17:38 GMT  
		Size: 79.7 MB (79738503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be06ac1c51e14a39e5f2458afb413c1ca3a4d5f0df7af98891c7c3ea59ff833`  
		Last Modified: Mon, 15 Jan 2018 22:17:23 GMT  
		Size: 2.7 KB (2736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920c7ffb77471e1abdfb9334d2f72ef1a7c9ba3aa0ec5c3ca4dfca8a7a8bff6d`  
		Last Modified: Mon, 15 Jan 2018 22:17:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
