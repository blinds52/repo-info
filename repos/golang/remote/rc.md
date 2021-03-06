## `golang:rc`

```console
$ docker pull golang@sha256:f764b99211b3d6f303bc2c5a8c6f72e2623faac86c9b5be2c157ced2f0e08cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.14393.2007; amd64
	-	windows version 10.0.16299.192; amd64

### `golang:rc` - linux; amd64

```console
$ docker pull golang@sha256:d91693da34090d9d14224a4e5ed6eb27a0900f05c01f32b3b60f6b88249883c9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (288041448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e97307ee2ff7a7a554278b38b7712e6816d6054545373c587f4b8ac4603567`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 07:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 11:21:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2018 01:59:55 GMT
ENV GOLANG_VERSION=1.10rc1
# Fri, 26 Jan 2018 02:00:09 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='c10d3cc7760bf3799037bd39027bbffdc568aea21d6fe60fe833373289c7b7c6' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='2c1ed86e3cbf9d9866333b73cee96a0cd0b8c73654f4705088caa64eb5a624d4' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='3a749faf38e80025b832dae250442ddc86d5bc353d752c781ea632e904922ff1' ;; 		i386) goRelArch='linux-386'; goRelSha256='03a98cc12b65dde36ed9561fa23530bcf5fa7ed85596aa74f2380f686fcbe928' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='f482c7d6193c23d36657f8f026a74222c82eeb443331c38bbf3493d971144988' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='a20d4077c0bb1d58710e48478ba0042950cf282f6ef1593aea4ac6e66265d22c' ;; 		*) goRelArch='src'; goRelSha256='743e97c856067f12fb39f1323d6e9956fb5f3339f0691d8749ecea553548ab03'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 26 Jan 2018 02:00:09 GMT
ENV GOPATH=/go
# Fri, 26 Jan 2018 02:00:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2018 02:00:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 26 Jan 2018 02:00:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50316693559041b3c6895bce352b10c302f31c074495671a820b689d2ce12baa`  
		Last Modified: Tue, 12 Dec 2017 08:04:27 GMT  
		Size: 50.0 MB (50022829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe52c89597fa1aac51f8ed83c481d0d5b269ab0f59a955168d69e9284ca46a8`  
		Last Modified: Tue, 12 Dec 2017 11:30:45 GMT  
		Size: 57.5 MB (57499152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bef1c9ad4d19d79e6ba6c7dfcc7fc69eee1f32e0f5ad3282989acca155965a`  
		Last Modified: Fri, 26 Jan 2018 02:15:40 GMT  
		Size: 120.0 MB (119954939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48765d3ca254c479beb8eb8920f581e83b0681bffcb5aa4a1e1a7bd46af7cf1b`  
		Last Modified: Fri, 26 Jan 2018 02:15:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc` - linux; arm variant v7

```console
$ docker pull golang@sha256:95e5cab87120334517ceaf697a0583be20d184e936a8c231323540c71be6400d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250824050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee97eaeafeb9d76dc4c348c707f89aeb635e83c36d6b7868c99099ff2e10d85a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 14:22:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2018 00:45:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2018 14:52:39 GMT
ENV GOLANG_VERSION=1.10rc1
# Fri, 26 Jan 2018 14:53:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='c10d3cc7760bf3799037bd39027bbffdc568aea21d6fe60fe833373289c7b7c6' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='2c1ed86e3cbf9d9866333b73cee96a0cd0b8c73654f4705088caa64eb5a624d4' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='3a749faf38e80025b832dae250442ddc86d5bc353d752c781ea632e904922ff1' ;; 		i386) goRelArch='linux-386'; goRelSha256='03a98cc12b65dde36ed9561fa23530bcf5fa7ed85596aa74f2380f686fcbe928' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='f482c7d6193c23d36657f8f026a74222c82eeb443331c38bbf3493d971144988' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='a20d4077c0bb1d58710e48478ba0042950cf282f6ef1593aea4ac6e66265d22c' ;; 		*) goRelArch='src'; goRelSha256='743e97c856067f12fb39f1323d6e9956fb5f3339f0691d8749ecea553548ab03'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 26 Jan 2018 14:53:50 GMT
ENV GOPATH=/go
# Fri, 26 Jan 2018 14:53:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2018 14:53:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 26 Jan 2018 14:53:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facba084babd0bca1fb6e0b05f34a2bc16a042cfdb3863d620dd87910bbe902e`  
		Last Modified: Tue, 12 Dec 2017 14:35:07 GMT  
		Size: 46.3 MB (46346753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518133f9a1c5b381ee53c0d58b1b9e3c78ed55a0b0c1ee8db9489858b86873b`  
		Last Modified: Sat, 20 Jan 2018 00:56:18 GMT  
		Size: 45.9 MB (45875393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa78fe6fd9a9d516afb4586ec34171dc200155c10c23fb02bf2ec27ec476ec3`  
		Last Modified: Fri, 26 Jan 2018 14:56:24 GMT  
		Size: 103.0 MB (103015031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b13b9fb79c44d1ae291037f32e8b6476fb7222f55e285bb53dfe0a9e3d39ca`  
		Last Modified: Fri, 26 Jan 2018 14:54:23 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:310c13c5391d689ce89565d70ccbfc8c1d6f02cf46a67369061bac157d1e8062
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256495714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe9cb273c5076b3b69f05e89747b0fefe98e152a8ca478fb571e58fc9833440`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 16:15:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 23:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2018 17:01:43 GMT
ENV GOLANG_VERSION=1.10rc1
# Fri, 26 Jan 2018 17:02:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='c10d3cc7760bf3799037bd39027bbffdc568aea21d6fe60fe833373289c7b7c6' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='2c1ed86e3cbf9d9866333b73cee96a0cd0b8c73654f4705088caa64eb5a624d4' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='3a749faf38e80025b832dae250442ddc86d5bc353d752c781ea632e904922ff1' ;; 		i386) goRelArch='linux-386'; goRelSha256='03a98cc12b65dde36ed9561fa23530bcf5fa7ed85596aa74f2380f686fcbe928' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='f482c7d6193c23d36657f8f026a74222c82eeb443331c38bbf3493d971144988' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='a20d4077c0bb1d58710e48478ba0042950cf282f6ef1593aea4ac6e66265d22c' ;; 		*) goRelArch='src'; goRelSha256='743e97c856067f12fb39f1323d6e9956fb5f3339f0691d8749ecea553548ab03'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 26 Jan 2018 17:02:06 GMT
ENV GOPATH=/go
# Fri, 26 Jan 2018 17:02:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2018 17:02:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 26 Jan 2018 17:02:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab5498df96eae5ccabdf778692dc41eeee09793f3792efadf0079545233069c`  
		Last Modified: Fri, 15 Dec 2017 17:19:55 GMT  
		Size: 48.0 MB (47983199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4e2722df7e740d51b766267b0ec38df71672a5b997802d45c67b8d0bdd2ce8`  
		Last Modified: Sat, 16 Dec 2017 00:01:51 GMT  
		Size: 48.9 MB (48935445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52c02f1682bc1f371e0f8da89f47a0850c69693d8c6d9160f3ec71244791308`  
		Last Modified: Fri, 26 Jan 2018 17:06:43 GMT  
		Size: 102.5 MB (102510058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939d5efb188ddb51618cf74e663be0eb42df4e35f45c22449a93e6f3b48ba51d`  
		Last Modified: Fri, 26 Jan 2018 17:06:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc` - linux; 386

```console
$ docker pull golang@sha256:a22b866c30dc1b6727f4dffec20bebd25f60c1696e6f7bce2cc21249b0b28486
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283434111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42de72c1d788422c3f25caaa4e25e202ecb0b856dd06017772c1203c93f65c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 14:47:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 16:56:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2018 06:17:40 GMT
ENV GOLANG_VERSION=1.10rc1
# Fri, 26 Jan 2018 06:18:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='c10d3cc7760bf3799037bd39027bbffdc568aea21d6fe60fe833373289c7b7c6' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='2c1ed86e3cbf9d9866333b73cee96a0cd0b8c73654f4705088caa64eb5a624d4' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='3a749faf38e80025b832dae250442ddc86d5bc353d752c781ea632e904922ff1' ;; 		i386) goRelArch='linux-386'; goRelSha256='03a98cc12b65dde36ed9561fa23530bcf5fa7ed85596aa74f2380f686fcbe928' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='f482c7d6193c23d36657f8f026a74222c82eeb443331c38bbf3493d971144988' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='a20d4077c0bb1d58710e48478ba0042950cf282f6ef1593aea4ac6e66265d22c' ;; 		*) goRelArch='src'; goRelSha256='743e97c856067f12fb39f1323d6e9956fb5f3339f0691d8749ecea553548ab03'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 26 Jan 2018 06:18:04 GMT
ENV GOPATH=/go
# Fri, 26 Jan 2018 06:18:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2018 06:18:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 26 Jan 2018 06:18:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff393180296f30b7b1cf94c5f67f82d434feb08eaff795346b0f5d3fe18c5ab6`  
		Last Modified: Wed, 13 Dec 2017 15:00:30 GMT  
		Size: 51.6 MB (51553695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c281e85d97666b881ac683415f45b31d0ccbdee55c6995710a9d10f4ae50fc`  
		Last Modified: Wed, 13 Dec 2017 17:08:28 GMT  
		Size: 62.0 MB (62034764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9b4eaf28832441fbf796f45d6e8c25aa26a8b8189df0ccc732a6ecf452e90b`  
		Last Modified: Fri, 26 Jan 2018 06:55:39 GMT  
		Size: 108.3 MB (108313428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64961327ef0e50749bba7d9a209ba52a57245c46670296f7a6e6b19a7ed062e`  
		Last Modified: Fri, 26 Jan 2018 06:55:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc` - linux; ppc64le

```console
$ docker pull golang@sha256:2fc5562c400b6872d310ca3ef6554948829e81ce8a3bc2ae33ff032156f6f0b3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264057827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cdbc478a10a331cc6114b359d22e65612aa735cbc6de47f83e11b339f232e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 03:37:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 09:22:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2018 05:08:34 GMT
ENV GOLANG_VERSION=1.10rc1
# Fri, 26 Jan 2018 05:09:00 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='c10d3cc7760bf3799037bd39027bbffdc568aea21d6fe60fe833373289c7b7c6' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='2c1ed86e3cbf9d9866333b73cee96a0cd0b8c73654f4705088caa64eb5a624d4' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='3a749faf38e80025b832dae250442ddc86d5bc353d752c781ea632e904922ff1' ;; 		i386) goRelArch='linux-386'; goRelSha256='03a98cc12b65dde36ed9561fa23530bcf5fa7ed85596aa74f2380f686fcbe928' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='f482c7d6193c23d36657f8f026a74222c82eeb443331c38bbf3493d971144988' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='a20d4077c0bb1d58710e48478ba0042950cf282f6ef1593aea4ac6e66265d22c' ;; 		*) goRelArch='src'; goRelSha256='743e97c856067f12fb39f1323d6e9956fb5f3339f0691d8749ecea553548ab03'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 26 Jan 2018 05:09:08 GMT
ENV GOPATH=/go
# Fri, 26 Jan 2018 05:09:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2018 05:09:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 26 Jan 2018 05:09:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90080349eff61f95b053aa65da87029e4c36cbccd1ac1d78002110d52ab56ba7`  
		Last Modified: Tue, 12 Dec 2017 03:56:07 GMT  
		Size: 50.0 MB (50029025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe942a3efef599ac5039d70fdad2f4d596c935116adeebd2024072d4b5f10c0`  
		Last Modified: Tue, 12 Dec 2017 09:34:02 GMT  
		Size: 52.7 MB (52710372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aebc2795423bcabc74937e17c59410e1d77a348aa003680e657d094158b8e5d`  
		Last Modified: Fri, 26 Jan 2018 05:12:40 GMT  
		Size: 101.3 MB (101307032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5f96ad63c2248a118944e6a4bf13a04f926add7f86e655d6fe2eefc23095b9`  
		Last Modified: Fri, 26 Jan 2018 05:12:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc` - linux; s390x

```console
$ docker pull golang@sha256:75551e6f425e02b85a0215981e5ca5ace452ced8a46b175a9720dae19ad97b4f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 MB (256957883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5f34cbe8ce864ae745f7fb8303b9c5f58101379e5e41d5a30ecce59bb8560f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 06:25:26 GMT
ADD file:52c2ff6c220e01ce9ef3bf8a808c3f51de553ffa707ffd3e664068af07974881 in / 
# Tue, 12 Dec 2017 06:25:27 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 06:58:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 06:58:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 06:59:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 09:42:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2018 11:39:27 GMT
ENV GOLANG_VERSION=1.10rc1
# Fri, 26 Jan 2018 11:39:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='c10d3cc7760bf3799037bd39027bbffdc568aea21d6fe60fe833373289c7b7c6' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='2c1ed86e3cbf9d9866333b73cee96a0cd0b8c73654f4705088caa64eb5a624d4' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='3a749faf38e80025b832dae250442ddc86d5bc353d752c781ea632e904922ff1' ;; 		i386) goRelArch='linux-386'; goRelSha256='03a98cc12b65dde36ed9561fa23530bcf5fa7ed85596aa74f2380f686fcbe928' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='f482c7d6193c23d36657f8f026a74222c82eeb443331c38bbf3493d971144988' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='a20d4077c0bb1d58710e48478ba0042950cf282f6ef1593aea4ac6e66265d22c' ;; 		*) goRelArch='src'; goRelSha256='743e97c856067f12fb39f1323d6e9956fb5f3339f0691d8749ecea553548ab03'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 26 Jan 2018 11:39:36 GMT
ENV GOPATH=/go
# Fri, 26 Jan 2018 11:39:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2018 11:39:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 26 Jan 2018 11:39:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:794821622a8cf94cd3f0f66e7708e7aed250701b9f626d2c58e22a73ca6869cf`  
		Last Modified: Tue, 12 Dec 2017 06:30:44 GMT  
		Size: 45.0 MB (44967073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff282cac5e026f80f2d55f6c7a510a9d2a8855bdde39824f93da04f1fd369475`  
		Last Modified: Tue, 12 Dec 2017 07:09:07 GMT  
		Size: 10.7 MB (10668313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04deb7c3aa54f0bb67511a855139b7d6eaeae932480fd568f7889597e870800f`  
		Last Modified: Tue, 12 Dec 2017 07:09:19 GMT  
		Size: 4.4 MB (4366027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd8efc8af21b5bb6284436d2189f0d8edb2eeade70328d44174c5cc870aec2`  
		Last Modified: Tue, 12 Dec 2017 07:10:10 GMT  
		Size: 50.4 MB (50448531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1364320336465b0c0c9ce49ceec734250fdb50c9a49a2af4a88ecf8f128580db`  
		Last Modified: Tue, 12 Dec 2017 09:45:33 GMT  
		Size: 45.8 MB (45814874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0736f565175224eed03b26f3065f71968a32bfb375fed208a9b2bc8b6a19dae2`  
		Last Modified: Fri, 26 Jan 2018 11:42:03 GMT  
		Size: 100.7 MB (100692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4c4e257db07da68b87fc89f68722d2e4bffed49710cf48077b7e669139cf15`  
		Last Modified: Fri, 26 Jan 2018 11:41:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc` - windows version 10.0.14393.2007; amd64

```console
$ docker pull golang@sha256:e43cceb307b37bbf5cf57e4c8608876e3a372759df58563ea697710051e96d3d
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 GB (5540727968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269cc076669c6f38fc5195980d94de7c496d4874f391f965427e6936b0cd604f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Thu, 04 Jan 2018 20:07:32 GMT
RUN Install update 10.0.14393.2007
# Fri, 05 Jan 2018 10:02:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Jan 2018 18:01:18 GMT
ENV GIT_VERSION=2.11.1
# Mon, 08 Jan 2018 18:01:19 GMT
ENV GIT_TAG=v2.11.1.windows.1
# Mon, 08 Jan 2018 18:01:20 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.11.1.windows.1/MinGit-2.11.1-64-bit.zip
# Mon, 08 Jan 2018 18:01:20 GMT
ENV GIT_DOWNLOAD_SHA256=668d16a799dd721ed126cc91bed49eb2c072ba1b25b50048280a4e2c5ed56e59
# Mon, 08 Jan 2018 18:03:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  git --version'; git --version; 		Write-Host 'Complete.';
# Mon, 08 Jan 2018 18:03:58 GMT
ENV GOPATH=C:\gopath
# Mon, 08 Jan 2018 18:05:10 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 26 Jan 2018 03:14:09 GMT
ENV GOLANG_VERSION=1.10rc1
# Fri, 26 Jan 2018 03:28:39 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'f3730ee5ff779a2a0862e858b94b40423c613e91142be99e05e47953343326a8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Fri, 26 Jan 2018 03:28:41 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 13 Dec 2016 10:53:31 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:449343c9d7e2919413898dc8a7e8780ef164b76a3b9dd19de104706edf05113a`  
		Last Modified: Thu, 04 Jan 2018 20:07:32 GMT  
		Size: 1.3 GB (1304019288 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c86d0434e36d69287bea586f96045245d5ee4f04e4e2a5edf6881dbbfdc628c3`  
		Last Modified: Fri, 05 Jan 2018 10:13:30 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb835a765d1adacc5e96f2684f32ef89614ccc4d5a99be32392b6b52c76ef46`  
		Last Modified: Mon, 08 Jan 2018 19:48:22 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f729550b3a7040ef71bf29aa3501c84f3dfb64ad061c41bc8d4a677a35cfdf`  
		Last Modified: Mon, 08 Jan 2018 19:48:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5421de1bee383e26bb9d4cab7e7f0991622bf7e7047bf93b7bebb8d8ac3354`  
		Last Modified: Mon, 08 Jan 2018 19:48:19 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680789f514fca4d05e20d2d49441bcb41dca2764a32a068b031fb7c851953342`  
		Last Modified: Mon, 08 Jan 2018 19:48:20 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7cac87c32591a7d201306b0f43d796071ecc6c2b11da97fa7b0a4a98203df9`  
		Last Modified: Mon, 08 Jan 2018 19:48:35 GMT  
		Size: 29.3 MB (29339650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081d4b636d0574daf16ae2a105d7b8b006786307281e608588ca203c00384996`  
		Last Modified: Mon, 08 Jan 2018 19:48:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d13313d01fe0e86343cdb272e265f9c10515bc522bdd3d8cb816c4b212f8a4`  
		Last Modified: Mon, 08 Jan 2018 19:48:18 GMT  
		Size: 4.9 MB (4874878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2e39d659913a4f63ac896fbb819db9f2ec7413b227e12d8a20176d54436a4b`  
		Last Modified: Fri, 26 Jan 2018 04:00:11 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ba8a614421e5e3f9fdcbb7a0c814369afc25b0b9b69e8fcf382c125c89480d`  
		Last Modified: Fri, 26 Jan 2018 04:01:36 GMT  
		Size: 132.5 MB (132498634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b98e86782cd3d4a1e3e2c1ab76ba8c1d971195b3da184ed5b2e45fa3edc9c5d`  
		Last Modified: Fri, 26 Jan 2018 04:00:10 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc` - windows version 10.0.16299.192; amd64

```console
$ docker pull golang@sha256:e883b1ad15700f875632b55a1481d38d017373aa7312e0ffe49b8523eef63000
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3129588731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81dd579ea26afe1abb7b4f81c19792611f496a239b11c5843951b17d224134a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 29 Sep 2017 14:43:28 GMT
RUN Apply image 10.0.16299.15
# Wed, 03 Jan 2018 04:46:54 GMT
RUN Install update 10.0.16299.192
# Mon, 08 Jan 2018 17:27:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Jan 2018 18:14:29 GMT
ENV GIT_VERSION=2.11.1
# Mon, 08 Jan 2018 18:14:29 GMT
ENV GIT_TAG=v2.11.1.windows.1
# Mon, 08 Jan 2018 18:14:30 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.11.1.windows.1/MinGit-2.11.1-64-bit.zip
# Mon, 08 Jan 2018 18:14:31 GMT
ENV GIT_DOWNLOAD_SHA256=668d16a799dd721ed126cc91bed49eb2c072ba1b25b50048280a4e2c5ed56e59
# Mon, 08 Jan 2018 18:17:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  git --version'; git --version; 		Write-Host 'Complete.';
# Mon, 08 Jan 2018 18:17:08 GMT
ENV GOPATH=C:\gopath
# Mon, 08 Jan 2018 18:17:59 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 26 Jan 2018 03:28:50 GMT
ENV GOLANG_VERSION=1.10rc1
# Sat, 27 Jan 2018 03:19:16 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'f3730ee5ff779a2a0862e858b94b40423c613e91142be99e05e47953343326a8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Sat, 27 Jan 2018 03:19:17 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:5847a47b8593f7c39aa5e3db09e50b76d42aa8898c0440c70cc9c69747d4c479`  
		Last Modified: Tue, 17 Oct 2017 15:51:05 GMT  
		Size: 2.3 GB (2274300585 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f887ccb8077bdc1f1fedd2da6066bb3542c528f5d103b40659ac25785ba4b9b`  
		Last Modified: Fri, 05 Jan 2018 19:38:30 GMT  
		Size: 689.7 MB (689720734 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:189c9822c1fc60043703fa16f44b1cab80d3a786d35bd6b61628d2b3f1fb9635`  
		Last Modified: Mon, 08 Jan 2018 17:34:16 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced016f882f58828f852af028c896ce147bb2b33b9d342b64f73d45720ceedd0`  
		Last Modified: Mon, 08 Jan 2018 19:52:05 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f21f168317cdc3c152749d966c0d43db4dc3535f9351d98dacdf0413afbcd7d`  
		Last Modified: Mon, 08 Jan 2018 19:52:04 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe305114696325373272c3f912e5ca4de2484a6c7534b892c4dea4b2ee5cae2`  
		Last Modified: Mon, 08 Jan 2018 19:52:03 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f37549f027d7629c2b600fc88dff293377dd5580bea22e016dcd849122f76`  
		Last Modified: Mon, 08 Jan 2018 19:52:01 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4655597d458099c45393834ed3bc33872b30b343ad2e0477f67472b5c9d1ea22`  
		Last Modified: Mon, 08 Jan 2018 19:52:18 GMT  
		Size: 29.0 MB (28956719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e4de5661145bcb63f11eb2c25c9d8b4a03d9ced31d0a6c992ada92bbafbfca`  
		Last Modified: Mon, 08 Jan 2018 19:52:00 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1ab2305863a8cd8304f89e0d8188b1072315a48130bb54bd5976fee044423f`  
		Last Modified: Mon, 08 Jan 2018 19:52:00 GMT  
		Size: 4.5 MB (4476553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69d6f76adb6ecbd2cd55c23e0d87cf1f646a50f2027d28da45e9328b9745857`  
		Last Modified: Sat, 27 Jan 2018 03:20:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c491596801063e424a7a4ad5c97abbb9e5e0bbc9274634b8856755c33476b0`  
		Last Modified: Sat, 27 Jan 2018 03:21:56 GMT  
		Size: 132.1 MB (132124444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3994357b88220eed30cf31ee9a6f757e517f651352fac6d83c4e65d17562f3`  
		Last Modified: Sat, 27 Jan 2018 03:20:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
