<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:3.12.1.3`](#aerospike31213)
-	[`aerospike:3.13.0.9`](#aerospike31309)
-	[`aerospike:3.14.1.7`](#aerospike31417)
-	[`aerospike:3.15.1.4`](#aerospike31514)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:3.12.1.3`

```console
$ docker pull aerospike@sha256:f90f420447d2e8542001aaf29244861e73353ec372d2bb15ef511451b74ede17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:3.12.1.3` - linux; amd64

```console
$ docker pull aerospike@sha256:81550a99a5e5db3340b0338143802edacd93da5cc91bb262c67bf600f16cb353
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69382343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fe79e2067f63b199a0b19363c1c21c398f75ae7176d657771f7d9f26de1d6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 25 Jan 2018 18:23:30 GMT
ADD file:a3344b835ea6fdc5692df23826c970403656c6947342e117b2ac1a05956679af in / 
# Thu, 25 Jan 2018 18:23:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Jan 2018 18:23:39 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2018 18:23:50 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Thu, 25 Jan 2018 18:23:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Jan 2018 18:23:51 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2018 18:56:43 GMT
ENV AEROSPIKE_VERSION=3.12.1.3
# Thu, 25 Jan 2018 18:56:44 GMT
ENV AEROSPIKE_SHA256=f72a143ea3c3daa1749923105978243679c8406f757457ec80b7577fe84c1dfc
# Thu, 25 Jan 2018 18:57:05 GMT
RUN apt-get update -y   && apt-get install -y wget python python-argparse python-bcrypt python-openssl logrotate net-tools iproute2 iputils-ping   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-ubuntu16.04.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && dpkg -r wget ca-certificates   && dpkg --purge wget ca-certificates   && apt-get purge -y
# Thu, 25 Jan 2018 18:57:06 GMT
COPY file:015e7cfae2aecd83035dfeb481a9485d5775175ecb59889f2b8f745c1ef60573 in /etc/aerospike/aerospike.conf 
# Thu, 25 Jan 2018 18:57:06 GMT
COPY file:864c89768f1d8390ee09d6490761795af49940cf8cbb62effbf84317a4e61cd2 in /entrypoint.sh 
# Thu, 25 Jan 2018 18:57:06 GMT
VOLUME [/opt/aerospike/data]
# Thu, 25 Jan 2018 18:57:07 GMT
EXPOSE 3000/tcp 3001/tcp 3002/tcp 3003/tcp
# Thu, 25 Jan 2018 18:57:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jan 2018 18:57:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:1be7f2b886e89a58e59c4e685fcc5905a26ddef3201f290b96f1eff7d778e122`  
		Last Modified: Wed, 24 Jan 2018 23:46:22 GMT  
		Size: 42.9 MB (42863496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbc4a21b806838b63b774b338c6ad19d696a9e655f50b4e358cc4006c3baa79`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a6f8e13782fed125f2247931c3eb20cc0e6428a5d79edb546f1f1405f0e49`  
		Last Modified: Thu, 25 Jan 2018 18:27:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be3072e5a37392e32f632bb234c0b461ff5675ab7e362afad6359fbd36884af`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c6d2f5970057aef3aef6da60f0fde280db1c077f0cd88ca33ec1a70a9c7b58`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af15979ee88a1117b2b2948b35a8897c54aeaa2bdcba26b7fb1a838222c4c115`  
		Last Modified: Thu, 25 Jan 2018 19:01:19 GMT  
		Size: 26.5 MB (26514869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078b49efaecd4d4bc0ceb987cd169d042bb9a32c99b7d2a77bca77a4af9d0dda`  
		Last Modified: Thu, 25 Jan 2018 19:01:11 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677819f157bf9a63301b7f67381ef1b274ee70aa98cc95ade82256e9add50a2d`  
		Last Modified: Thu, 25 Jan 2018 19:01:09 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:3.13.0.9`

```console
$ docker pull aerospike@sha256:deb535aa9f64e4d90ec594f50e5e7eea295f1ebc83a062f3757def67e7603f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:3.13.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:105a0833aaf1b4ecade191a9a3444f2010342db57c7cb471280364bcca8349e0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69756860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0fecfc3888f71b2c2076a70fca1d26742cdc05ae721e896fc43c882513cf4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 25 Jan 2018 18:23:30 GMT
ADD file:a3344b835ea6fdc5692df23826c970403656c6947342e117b2ac1a05956679af in / 
# Thu, 25 Jan 2018 18:23:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Jan 2018 18:23:39 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2018 18:23:50 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Thu, 25 Jan 2018 18:23:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Jan 2018 18:23:51 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2018 18:57:31 GMT
ENV AEROSPIKE_VERSION=3.13.0.9
# Thu, 25 Jan 2018 18:57:32 GMT
ENV AEROSPIKE_SHA256=cea81b59fca99168d6be9159dff439cc242bbf1a162e960647bdceb1ced46752
# Thu, 25 Jan 2018 18:57:51 GMT
RUN apt-get update -y   && apt-get install -y wget python python-argparse python-bcrypt python-openssl logrotate net-tools iproute2 iputils-ping   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-ubuntu16.04.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && dpkg -r wget ca-certificates   && dpkg --purge wget ca-certificates   && apt-get purge -y
# Thu, 25 Jan 2018 18:57:51 GMT
COPY file:015e7cfae2aecd83035dfeb481a9485d5775175ecb59889f2b8f745c1ef60573 in /etc/aerospike/aerospike.conf 
# Thu, 25 Jan 2018 18:57:52 GMT
COPY file:864c89768f1d8390ee09d6490761795af49940cf8cbb62effbf84317a4e61cd2 in /entrypoint.sh 
# Thu, 25 Jan 2018 18:57:52 GMT
VOLUME [/opt/aerospike/data]
# Thu, 25 Jan 2018 18:57:52 GMT
EXPOSE 3000/tcp 3001/tcp 3002/tcp 3003/tcp
# Thu, 25 Jan 2018 18:57:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jan 2018 18:57:53 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:1be7f2b886e89a58e59c4e685fcc5905a26ddef3201f290b96f1eff7d778e122`  
		Last Modified: Wed, 24 Jan 2018 23:46:22 GMT  
		Size: 42.9 MB (42863496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbc4a21b806838b63b774b338c6ad19d696a9e655f50b4e358cc4006c3baa79`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a6f8e13782fed125f2247931c3eb20cc0e6428a5d79edb546f1f1405f0e49`  
		Last Modified: Thu, 25 Jan 2018 18:27:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be3072e5a37392e32f632bb234c0b461ff5675ab7e362afad6359fbd36884af`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c6d2f5970057aef3aef6da60f0fde280db1c077f0cd88ca33ec1a70a9c7b58`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd8d722dfb119434b642f5b0dd64b1ea94cbdefcf88e338a78743ee0be175cc`  
		Last Modified: Thu, 25 Jan 2018 19:01:43 GMT  
		Size: 26.9 MB (26889389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065838c121932534a7fc26e3b86c5ddde33c355f35fae8017f717b678a2ec935`  
		Last Modified: Thu, 25 Jan 2018 19:01:38 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8119f0cc377e36f2a32af04d40615a4e14b5003fd0086daad983a40f6d41d49b`  
		Last Modified: Thu, 25 Jan 2018 19:01:37 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:3.14.1.7`

```console
$ docker pull aerospike@sha256:62786fdc8066b546d04a32761ecfcca94bcbd2057de21c1aefdbf892fbc80346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:3.14.1.7` - linux; amd64

```console
$ docker pull aerospike@sha256:5649c3d3921c9d5199d2a89fb3710519d5cee43c475a51338a4450225ea2d20d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69331716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bb9160f926748ceadaec36b780dc866911c4a2dbc54cf6909aca98d7fcd4e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 25 Jan 2018 18:23:30 GMT
ADD file:a3344b835ea6fdc5692df23826c970403656c6947342e117b2ac1a05956679af in / 
# Thu, 25 Jan 2018 18:23:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Jan 2018 18:23:39 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2018 18:23:50 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Thu, 25 Jan 2018 18:23:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Jan 2018 18:23:51 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2018 18:58:07 GMT
ENV AEROSPIKE_VERSION=3.14.1.7
# Thu, 25 Jan 2018 18:58:07 GMT
ENV AEROSPIKE_SHA256=6addd009684a58b16be5bfbfccd87d70a5c9e6c2c3e6ac3c77f82949dacc101e
# Thu, 25 Jan 2018 18:58:26 GMT
RUN apt-get update -y   && apt-get install -y wget python python-argparse python-bcrypt python-openssl logrotate net-tools iproute2 iputils-ping   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-ubuntu16.04.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && dpkg -r wget ca-certificates   && dpkg --purge wget ca-certificates   && apt-get purge -y
# Thu, 25 Jan 2018 18:58:26 GMT
COPY file:015e7cfae2aecd83035dfeb481a9485d5775175ecb59889f2b8f745c1ef60573 in /etc/aerospike/aerospike.conf 
# Thu, 25 Jan 2018 18:58:27 GMT
COPY file:864c89768f1d8390ee09d6490761795af49940cf8cbb62effbf84317a4e61cd2 in /entrypoint.sh 
# Thu, 25 Jan 2018 18:58:27 GMT
VOLUME [/opt/aerospike/data]
# Thu, 25 Jan 2018 18:58:27 GMT
EXPOSE 3000/tcp 3001/tcp 3002/tcp 3003/tcp
# Thu, 25 Jan 2018 18:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jan 2018 18:58:28 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:1be7f2b886e89a58e59c4e685fcc5905a26ddef3201f290b96f1eff7d778e122`  
		Last Modified: Wed, 24 Jan 2018 23:46:22 GMT  
		Size: 42.9 MB (42863496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbc4a21b806838b63b774b338c6ad19d696a9e655f50b4e358cc4006c3baa79`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a6f8e13782fed125f2247931c3eb20cc0e6428a5d79edb546f1f1405f0e49`  
		Last Modified: Thu, 25 Jan 2018 18:27:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be3072e5a37392e32f632bb234c0b461ff5675ab7e362afad6359fbd36884af`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c6d2f5970057aef3aef6da60f0fde280db1c077f0cd88ca33ec1a70a9c7b58`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeaa1aace3a5ea70dbb77f3532f6967f419a1029f173a3d7963d88caa8ccb3`  
		Last Modified: Thu, 25 Jan 2018 19:02:09 GMT  
		Size: 26.5 MB (26464243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f21559732c5730ef152af7d8039063081c0ae2358b408c3f15b5cac4bb40c`  
		Last Modified: Thu, 25 Jan 2018 19:02:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7027af2122b42079ffbc8f3aa0e4e5d5f7baafe361a49b1b9cdfb25feeb6f0`  
		Last Modified: Thu, 25 Jan 2018 19:02:05 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:3.15.1.4`

```console
$ docker pull aerospike@sha256:f69226bfde1303c104bd26960bd18d7c87ea7562f48f3c213553481ba89c58bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:3.15.1.4` - linux; amd64

```console
$ docker pull aerospike@sha256:29868eb3d797b18f0d2e4768639b28c078fe0a9ab11dc0350d5e57e5b4532147
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68733137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6cff6d63613b18d154b18171d38f837afc256f324802da95f2b15add114f6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 25 Jan 2018 18:23:30 GMT
ADD file:a3344b835ea6fdc5692df23826c970403656c6947342e117b2ac1a05956679af in / 
# Thu, 25 Jan 2018 18:23:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Jan 2018 18:23:39 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2018 18:23:50 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Thu, 25 Jan 2018 18:23:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Jan 2018 18:23:51 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2018 18:59:54 GMT
ENV AEROSPIKE_VERSION=3.15.1.4
# Thu, 25 Jan 2018 18:59:55 GMT
ENV AEROSPIKE_SHA256=9b533226d4cc5473fc25f6cc4f81fdd5ba0864aeedef7adf14bdaa4ff1a73b2b
# Thu, 25 Jan 2018 19:00:21 GMT
RUN apt-get update -y   && apt-get install -y wget python python-argparse python-bcrypt python-openssl logrotate net-tools iproute2 iputils-ping   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-ubuntu16.04.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && dpkg -r wget ca-certificates   && dpkg --purge wget ca-certificates   && apt-get purge -y
# Thu, 25 Jan 2018 19:00:30 GMT
COPY file:015e7cfae2aecd83035dfeb481a9485d5775175ecb59889f2b8f745c1ef60573 in /etc/aerospike/aerospike.conf 
# Thu, 25 Jan 2018 19:00:30 GMT
COPY file:864c89768f1d8390ee09d6490761795af49940cf8cbb62effbf84317a4e61cd2 in /entrypoint.sh 
# Thu, 25 Jan 2018 19:00:31 GMT
VOLUME [/opt/aerospike/data]
# Thu, 25 Jan 2018 19:00:31 GMT
EXPOSE 3000/tcp 3001/tcp 3002/tcp 3003/tcp
# Thu, 25 Jan 2018 19:00:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jan 2018 19:00:42 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:1be7f2b886e89a58e59c4e685fcc5905a26ddef3201f290b96f1eff7d778e122`  
		Last Modified: Wed, 24 Jan 2018 23:46:22 GMT  
		Size: 42.9 MB (42863496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbc4a21b806838b63b774b338c6ad19d696a9e655f50b4e358cc4006c3baa79`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a6f8e13782fed125f2247931c3eb20cc0e6428a5d79edb546f1f1405f0e49`  
		Last Modified: Thu, 25 Jan 2018 18:27:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be3072e5a37392e32f632bb234c0b461ff5675ab7e362afad6359fbd36884af`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c6d2f5970057aef3aef6da60f0fde280db1c077f0cd88ca33ec1a70a9c7b58`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d41300b17e424a21bfccb63bdf509cbd0daa5d350f5302665a947e20e7edd3`  
		Last Modified: Thu, 25 Jan 2018 19:02:35 GMT  
		Size: 25.9 MB (25865664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea45ece798036633341a459ae059f64e2ff5b310360ecb0a041608892ae02ddb`  
		Last Modified: Thu, 25 Jan 2018 19:02:30 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc4b1f6135ba1f726c6eb4301e893c9be0613fc1af2a395136cff28c058dbe2`  
		Last Modified: Thu, 25 Jan 2018 19:02:29 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:f69226bfde1303c104bd26960bd18d7c87ea7562f48f3c213553481ba89c58bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:29868eb3d797b18f0d2e4768639b28c078fe0a9ab11dc0350d5e57e5b4532147
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68733137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6cff6d63613b18d154b18171d38f837afc256f324802da95f2b15add114f6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 25 Jan 2018 18:23:30 GMT
ADD file:a3344b835ea6fdc5692df23826c970403656c6947342e117b2ac1a05956679af in / 
# Thu, 25 Jan 2018 18:23:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Jan 2018 18:23:39 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2018 18:23:50 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Thu, 25 Jan 2018 18:23:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Jan 2018 18:23:51 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2018 18:59:54 GMT
ENV AEROSPIKE_VERSION=3.15.1.4
# Thu, 25 Jan 2018 18:59:55 GMT
ENV AEROSPIKE_SHA256=9b533226d4cc5473fc25f6cc4f81fdd5ba0864aeedef7adf14bdaa4ff1a73b2b
# Thu, 25 Jan 2018 19:00:21 GMT
RUN apt-get update -y   && apt-get install -y wget python python-argparse python-bcrypt python-openssl logrotate net-tools iproute2 iputils-ping   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-ubuntu16.04.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && dpkg -r wget ca-certificates   && dpkg --purge wget ca-certificates   && apt-get purge -y
# Thu, 25 Jan 2018 19:00:30 GMT
COPY file:015e7cfae2aecd83035dfeb481a9485d5775175ecb59889f2b8f745c1ef60573 in /etc/aerospike/aerospike.conf 
# Thu, 25 Jan 2018 19:00:30 GMT
COPY file:864c89768f1d8390ee09d6490761795af49940cf8cbb62effbf84317a4e61cd2 in /entrypoint.sh 
# Thu, 25 Jan 2018 19:00:31 GMT
VOLUME [/opt/aerospike/data]
# Thu, 25 Jan 2018 19:00:31 GMT
EXPOSE 3000/tcp 3001/tcp 3002/tcp 3003/tcp
# Thu, 25 Jan 2018 19:00:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jan 2018 19:00:42 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:1be7f2b886e89a58e59c4e685fcc5905a26ddef3201f290b96f1eff7d778e122`  
		Last Modified: Wed, 24 Jan 2018 23:46:22 GMT  
		Size: 42.9 MB (42863496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbc4a21b806838b63b774b338c6ad19d696a9e655f50b4e358cc4006c3baa79`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a6f8e13782fed125f2247931c3eb20cc0e6428a5d79edb546f1f1405f0e49`  
		Last Modified: Thu, 25 Jan 2018 18:27:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be3072e5a37392e32f632bb234c0b461ff5675ab7e362afad6359fbd36884af`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c6d2f5970057aef3aef6da60f0fde280db1c077f0cd88ca33ec1a70a9c7b58`  
		Last Modified: Thu, 25 Jan 2018 18:27:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d41300b17e424a21bfccb63bdf509cbd0daa5d350f5302665a947e20e7edd3`  
		Last Modified: Thu, 25 Jan 2018 19:02:35 GMT  
		Size: 25.9 MB (25865664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea45ece798036633341a459ae059f64e2ff5b310360ecb0a041608892ae02ddb`  
		Last Modified: Thu, 25 Jan 2018 19:02:30 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc4b1f6135ba1f726c6eb4301e893c9be0613fc1af2a395136cff28c058dbe2`  
		Last Modified: Thu, 25 Jan 2018 19:02:29 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
