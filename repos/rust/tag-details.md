<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rust`

-	[`rust:1`](#rust1)
-	[`rust:1.23`](#rust123)
-	[`rust:1.23.0`](#rust1230)
-	[`rust:1.23.0-jessie`](#rust1230-jessie)
-	[`rust:1.23.0-stretch`](#rust1230-stretch)
-	[`rust:1.23-jessie`](#rust123-jessie)
-	[`rust:1.23-stretch`](#rust123-stretch)
-	[`rust:1-jessie`](#rust1-jessie)
-	[`rust:1-stretch`](#rust1-stretch)
-	[`rust:jessie`](#rustjessie)
-	[`rust:latest`](#rustlatest)
-	[`rust:stretch`](#ruststretch)

## `rust:1`

```console
$ docker pull rust@sha256:98b208cc6c5996bd3c4cf580a076e8b070d2916f243057dc6b7f9770c54bd58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1` - linux; amd64

```console
$ docker pull rust@sha256:f087d993dce386920e0ebe72411b755b5827abc441581d9964dd39eeae6d52b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.1 MB (510064070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f381373aec8d0033cd25bdab8f641b4c847dc2f738432133620c33076b07ed`
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
# Tue, 12 Dec 2017 07:56:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:13:12 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:0f46f97746e4df5959e8c821ca69fdd6c0bedd611c1e0ab3b6970f7202b9bb10`  
		Last Modified: Tue, 12 Dec 2017 08:05:32 GMT  
		Size: 213.1 MB (213085177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3767d6ece93daba294352c76824377023d5b88fa8841d362ac4fcd5aa2f031`  
		Last Modified: Thu, 04 Jan 2018 19:34:05 GMT  
		Size: 186.4 MB (186391661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:4295abe2158b5f0648a51a9b5499642b7ff365b62afe0bce0f470871fe39f8a8
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.5 MB (470469897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab6533f9a6de2edeaf144f8af5d45e354191989de2af398b065ac7ddaa8a25`
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
# Tue, 12 Dec 2017 14:24:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:16:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:25:18 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:6b98be7e69ceba1d8ac982eeed4ed62c19e27b2ecff5a4e00df3e9e5add17b9c`  
		Last Modified: Tue, 12 Dec 2017 14:36:34 GMT  
		Size: 193.9 MB (193909280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2edc30150366daf2b75a4c16b463dfcca1946afee4aa8b9b2c668d14b87430`  
		Last Modified: Fri, 05 Jan 2018 16:27:02 GMT  
		Size: 174.6 MB (174627147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28398c3e11a206b5e83353c755a901ddc42252cd6fcf9d419b6ef2b2e2641764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477037975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539a3f74443cb8b611b6fb779294a77f508f464bbaebd21aa5d19801957ce784`
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
# Fri, 15 Dec 2017 16:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:31:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:48:42 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:b898d058564c6e8f16b8d652e13a9e6a522a70394c4337ef428e6ad430f91804`  
		Last Modified: Fri, 15 Dec 2017 17:21:15 GMT  
		Size: 200.5 MB (200539864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73655033400cbd3c9785ae0f5cfa85389c87b87fbc727a627e8921f8c7e5e278`  
		Last Modified: Fri, 05 Jan 2018 00:51:23 GMT  
		Size: 171.4 MB (171448026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:3c212bbd0df19dee588a2f60a05ca96db7c5fa4163fcd36d9536c6ce077ef553
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511429084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd26453ae35b0775b750a202b1aff88972467ae9946e50e527844a2f61cd849`
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
# Wed, 13 Dec 2017 14:50:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 16:37:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:11:28 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:8ea5318279c9f2c159ea30e29a11732815fc890ad4c36bd02c273984d19a6224`  
		Last Modified: Wed, 13 Dec 2017 15:02:14 GMT  
		Size: 218.2 MB (218187101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db2a56de0016046b36fe953a17bc7f35813b80fde80a6b5839293006ccb1e0`  
		Last Modified: Fri, 05 Jan 2018 05:31:12 GMT  
		Size: 180.2 MB (180156190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.23`

```console
$ docker pull rust@sha256:98b208cc6c5996bd3c4cf580a076e8b070d2916f243057dc6b7f9770c54bd58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.23` - linux; amd64

```console
$ docker pull rust@sha256:f087d993dce386920e0ebe72411b755b5827abc441581d9964dd39eeae6d52b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.1 MB (510064070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f381373aec8d0033cd25bdab8f641b4c847dc2f738432133620c33076b07ed`
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
# Tue, 12 Dec 2017 07:56:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:13:12 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:0f46f97746e4df5959e8c821ca69fdd6c0bedd611c1e0ab3b6970f7202b9bb10`  
		Last Modified: Tue, 12 Dec 2017 08:05:32 GMT  
		Size: 213.1 MB (213085177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3767d6ece93daba294352c76824377023d5b88fa8841d362ac4fcd5aa2f031`  
		Last Modified: Thu, 04 Jan 2018 19:34:05 GMT  
		Size: 186.4 MB (186391661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23` - linux; arm variant v7

```console
$ docker pull rust@sha256:4295abe2158b5f0648a51a9b5499642b7ff365b62afe0bce0f470871fe39f8a8
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.5 MB (470469897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab6533f9a6de2edeaf144f8af5d45e354191989de2af398b065ac7ddaa8a25`
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
# Tue, 12 Dec 2017 14:24:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:16:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:25:18 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:6b98be7e69ceba1d8ac982eeed4ed62c19e27b2ecff5a4e00df3e9e5add17b9c`  
		Last Modified: Tue, 12 Dec 2017 14:36:34 GMT  
		Size: 193.9 MB (193909280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2edc30150366daf2b75a4c16b463dfcca1946afee4aa8b9b2c668d14b87430`  
		Last Modified: Fri, 05 Jan 2018 16:27:02 GMT  
		Size: 174.6 MB (174627147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28398c3e11a206b5e83353c755a901ddc42252cd6fcf9d419b6ef2b2e2641764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477037975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539a3f74443cb8b611b6fb779294a77f508f464bbaebd21aa5d19801957ce784`
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
# Fri, 15 Dec 2017 16:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:31:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:48:42 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:b898d058564c6e8f16b8d652e13a9e6a522a70394c4337ef428e6ad430f91804`  
		Last Modified: Fri, 15 Dec 2017 17:21:15 GMT  
		Size: 200.5 MB (200539864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73655033400cbd3c9785ae0f5cfa85389c87b87fbc727a627e8921f8c7e5e278`  
		Last Modified: Fri, 05 Jan 2018 00:51:23 GMT  
		Size: 171.4 MB (171448026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23` - linux; 386

```console
$ docker pull rust@sha256:3c212bbd0df19dee588a2f60a05ca96db7c5fa4163fcd36d9536c6ce077ef553
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511429084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd26453ae35b0775b750a202b1aff88972467ae9946e50e527844a2f61cd849`
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
# Wed, 13 Dec 2017 14:50:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 16:37:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:11:28 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:8ea5318279c9f2c159ea30e29a11732815fc890ad4c36bd02c273984d19a6224`  
		Last Modified: Wed, 13 Dec 2017 15:02:14 GMT  
		Size: 218.2 MB (218187101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db2a56de0016046b36fe953a17bc7f35813b80fde80a6b5839293006ccb1e0`  
		Last Modified: Fri, 05 Jan 2018 05:31:12 GMT  
		Size: 180.2 MB (180156190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.23.0`

```console
$ docker pull rust@sha256:98b208cc6c5996bd3c4cf580a076e8b070d2916f243057dc6b7f9770c54bd58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.23.0` - linux; amd64

```console
$ docker pull rust@sha256:f087d993dce386920e0ebe72411b755b5827abc441581d9964dd39eeae6d52b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.1 MB (510064070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f381373aec8d0033cd25bdab8f641b4c847dc2f738432133620c33076b07ed`
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
# Tue, 12 Dec 2017 07:56:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:13:12 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:0f46f97746e4df5959e8c821ca69fdd6c0bedd611c1e0ab3b6970f7202b9bb10`  
		Last Modified: Tue, 12 Dec 2017 08:05:32 GMT  
		Size: 213.1 MB (213085177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3767d6ece93daba294352c76824377023d5b88fa8841d362ac4fcd5aa2f031`  
		Last Modified: Thu, 04 Jan 2018 19:34:05 GMT  
		Size: 186.4 MB (186391661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:4295abe2158b5f0648a51a9b5499642b7ff365b62afe0bce0f470871fe39f8a8
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.5 MB (470469897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab6533f9a6de2edeaf144f8af5d45e354191989de2af398b065ac7ddaa8a25`
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
# Tue, 12 Dec 2017 14:24:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:16:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:25:18 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:6b98be7e69ceba1d8ac982eeed4ed62c19e27b2ecff5a4e00df3e9e5add17b9c`  
		Last Modified: Tue, 12 Dec 2017 14:36:34 GMT  
		Size: 193.9 MB (193909280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2edc30150366daf2b75a4c16b463dfcca1946afee4aa8b9b2c668d14b87430`  
		Last Modified: Fri, 05 Jan 2018 16:27:02 GMT  
		Size: 174.6 MB (174627147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28398c3e11a206b5e83353c755a901ddc42252cd6fcf9d419b6ef2b2e2641764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477037975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539a3f74443cb8b611b6fb779294a77f508f464bbaebd21aa5d19801957ce784`
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
# Fri, 15 Dec 2017 16:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:31:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:48:42 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:b898d058564c6e8f16b8d652e13a9e6a522a70394c4337ef428e6ad430f91804`  
		Last Modified: Fri, 15 Dec 2017 17:21:15 GMT  
		Size: 200.5 MB (200539864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73655033400cbd3c9785ae0f5cfa85389c87b87fbc727a627e8921f8c7e5e278`  
		Last Modified: Fri, 05 Jan 2018 00:51:23 GMT  
		Size: 171.4 MB (171448026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23.0` - linux; 386

```console
$ docker pull rust@sha256:3c212bbd0df19dee588a2f60a05ca96db7c5fa4163fcd36d9536c6ce077ef553
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511429084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd26453ae35b0775b750a202b1aff88972467ae9946e50e527844a2f61cd849`
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
# Wed, 13 Dec 2017 14:50:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 16:37:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:11:28 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:8ea5318279c9f2c159ea30e29a11732815fc890ad4c36bd02c273984d19a6224`  
		Last Modified: Wed, 13 Dec 2017 15:02:14 GMT  
		Size: 218.2 MB (218187101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db2a56de0016046b36fe953a17bc7f35813b80fde80a6b5839293006ccb1e0`  
		Last Modified: Fri, 05 Jan 2018 05:31:12 GMT  
		Size: 180.2 MB (180156190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.23.0-jessie`

```console
$ docker pull rust@sha256:ebda1a950dfd49b3a81a26c408fa5d3b489ee1c762269778d1c5000b88040fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.23.0-jessie` - linux; amd64

```console
$ docker pull rust@sha256:e3bf7ac34b74167e585c0051ff31c1796ee6cd0de34f7865896fc6a51753f6b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.5 MB (436478181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b100402c3b158e162487b17df82aeef19abbbdd3d6e1ca2098fcca18dab3a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:49:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:49:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 07:49:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:50:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:41 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:23:30 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b491c575b06601bb07a2d88bfc3ace6c6005edc1b4d8da3ba6e37e04e9592d6`  
		Last Modified: Tue, 12 Dec 2017 08:00:34 GMT  
		Size: 19.3 MB (19266203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b313b08bab3b8bbcf0de4171a2a80a01e67fab094f272819b76a58705d21ab28`  
		Last Modified: Tue, 12 Dec 2017 08:01:02 GMT  
		Size: 43.3 MB (43253338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d6678c3f0e0c6e2b58b51ad100912b7c0e4dfedf98a1808417216fd5d948e5`  
		Last Modified: Tue, 12 Dec 2017 08:01:40 GMT  
		Size: 135.0 MB (134968174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dd223b09f7ea917286f36585be6d664242342970092b20c566ce39799eb2d8`  
		Last Modified: Thu, 04 Jan 2018 19:43:32 GMT  
		Size: 186.4 MB (186390769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23.0-jessie` - linux; arm variant v7

```console
$ docker pull rust@sha256:00c3bf85b3ffdc36fe337d904c0f9fd0f2bda45d7433efd767fc13775a363002
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.4 MB (395368827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed9280211bee90c7cf29b1a367a8ef3e9a241b1c2901be89053311d9c50fd4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 13:27:05 GMT
ADD file:aeb57f3a84dc1b93e1d38a80409a407df553344149d5070ed79b656865c90c54 in / 
# Tue, 12 Dec 2017 13:27:06 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:14:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:14:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 14:15:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:17:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:18:29 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:26:00 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:95e140a16c792899abc97cadee0138064dd21346fe51aa332ca4cbbd5563383c`  
		Last Modified: Tue, 12 Dec 2017 13:38:47 GMT  
		Size: 48.7 MB (48691755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237499cbbf2c5155fadc128c997700f0c5ec6355ba9704d0ec3f81c29640c9c4`  
		Last Modified: Tue, 12 Dec 2017 14:30:53 GMT  
		Size: 18.3 MB (18265038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f718f16c2f9a8213b99fcb49e72dad0036d1426f09c089f1e389b684f26520`  
		Last Modified: Tue, 12 Dec 2017 14:31:23 GMT  
		Size: 39.7 MB (39727713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affc0d5be2fb6b1dbb9d86ff0f533d88026215828cb4b1893257572ebf86f8d2`  
		Last Modified: Tue, 12 Dec 2017 14:32:10 GMT  
		Size: 114.1 MB (114057010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8af88c0d3aafa806ad2c595cce96fb2a7bddae9c3b74079ff185da9bbcd459`  
		Last Modified: Fri, 05 Jan 2018 16:28:26 GMT  
		Size: 174.6 MB (174627311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23.0-jessie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:df79b88460d9f7df06539a66dab1ef7e35a17645fbd8e258a9982f25c3aa3551
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397061702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795b0bd90a7734e1e4b207b3bb9870da0865fcf74e3c6ed492899ebcaba45092`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 18:24:58 GMT
ADD file:f0da52be154f821919dcbfb92afd89714053ae507038126715c96ac77a6768e1 in / 
# Tue, 12 Dec 2017 18:24:59 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 15:52:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 15:52:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 15:54:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:01:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:32:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:50:01 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:7e6d91e96b32c4999458c6c0cda42f920e41aab0cfbf3153f6e013b222bf084d`  
		Last Modified: Tue, 12 Dec 2017 18:39:54 GMT  
		Size: 49.9 MB (49926676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f2d61ff35851bad52cd6e85a1aa2c7b986069f0e062b7199ea07bc705f60cc`  
		Last Modified: Fri, 15 Dec 2017 17:15:45 GMT  
		Size: 18.7 MB (18739771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113d3a736bdb3c71bbdebc354892ca5b3e58753ed7a23231f8335c9ef0dc4a2`  
		Last Modified: Fri, 15 Dec 2017 17:16:09 GMT  
		Size: 41.0 MB (41021189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cf756b1b5f041ca4a78dc397a47f650ce6012584924a41c96fdf5da2edd2dc`  
		Last Modified: Fri, 15 Dec 2017 17:16:55 GMT  
		Size: 115.9 MB (115925986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1feb78ef2611564247fce161f72b48441e3a464f9924017cc96cd3392a76e16`  
		Last Modified: Fri, 05 Jan 2018 00:53:30 GMT  
		Size: 171.4 MB (171448080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23.0-jessie` - linux; 386

```console
$ docker pull rust@sha256:327631815fd6aff2bbdc6de73586f82a148d1f9439c24015b524bb7bc7bac08c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 MB (433592766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b111969f24678ebfcbb38c9bdca3bd9825860519dd54e8a73f47206c3d4b15`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 14:19:55 GMT
ADD file:235a40e05b677eb2ae7e7a3cc5cbb0cda242ff15dddb87cb8dc9bb0cd2d6aed8 in / 
# Tue, 12 Dec 2017 14:19:55 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 16:53:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 16:53:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 16:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 16:56:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 20:23:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:20:57 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d99577c7ee3d4d82987bedaeb10f3244ff7e19e41c5259bb8cac00568d1c4271`  
		Last Modified: Tue, 12 Dec 2017 14:46:26 GMT  
		Size: 52.8 MB (52777369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94aafa6d6f35f82e1fdc93cd4f7f6ab829f6297c8defaaa911dfb2de063bf3d`  
		Last Modified: Tue, 12 Dec 2017 17:27:39 GMT  
		Size: 21.6 MB (21596374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd19391b0ebd36e15e21cb3a6728c5950937634b9c81ecc7e3d1422b1dc25eb`  
		Last Modified: Tue, 12 Dec 2017 17:28:18 GMT  
		Size: 43.9 MB (43918299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8333879ca1894c745f67c724a7e4ad35542f5966a47bb050928910a944130ea0`  
		Last Modified: Tue, 12 Dec 2017 17:29:10 GMT  
		Size: 135.1 MB (135144789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d89f6a0e149d67f583d88c42593cf41d53d93a623aa6870162b8c32ec94ff`  
		Last Modified: Fri, 05 Jan 2018 05:43:12 GMT  
		Size: 180.2 MB (180155935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.23.0-stretch`

```console
$ docker pull rust@sha256:98b208cc6c5996bd3c4cf580a076e8b070d2916f243057dc6b7f9770c54bd58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.23.0-stretch` - linux; amd64

```console
$ docker pull rust@sha256:f087d993dce386920e0ebe72411b755b5827abc441581d9964dd39eeae6d52b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.1 MB (510064070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f381373aec8d0033cd25bdab8f641b4c847dc2f738432133620c33076b07ed`
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
# Tue, 12 Dec 2017 07:56:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:13:12 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:0f46f97746e4df5959e8c821ca69fdd6c0bedd611c1e0ab3b6970f7202b9bb10`  
		Last Modified: Tue, 12 Dec 2017 08:05:32 GMT  
		Size: 213.1 MB (213085177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3767d6ece93daba294352c76824377023d5b88fa8841d362ac4fcd5aa2f031`  
		Last Modified: Thu, 04 Jan 2018 19:34:05 GMT  
		Size: 186.4 MB (186391661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23.0-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:4295abe2158b5f0648a51a9b5499642b7ff365b62afe0bce0f470871fe39f8a8
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.5 MB (470469897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab6533f9a6de2edeaf144f8af5d45e354191989de2af398b065ac7ddaa8a25`
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
# Tue, 12 Dec 2017 14:24:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:16:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:25:18 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:6b98be7e69ceba1d8ac982eeed4ed62c19e27b2ecff5a4e00df3e9e5add17b9c`  
		Last Modified: Tue, 12 Dec 2017 14:36:34 GMT  
		Size: 193.9 MB (193909280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2edc30150366daf2b75a4c16b463dfcca1946afee4aa8b9b2c668d14b87430`  
		Last Modified: Fri, 05 Jan 2018 16:27:02 GMT  
		Size: 174.6 MB (174627147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23.0-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28398c3e11a206b5e83353c755a901ddc42252cd6fcf9d419b6ef2b2e2641764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477037975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539a3f74443cb8b611b6fb779294a77f508f464bbaebd21aa5d19801957ce784`
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
# Fri, 15 Dec 2017 16:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:31:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:48:42 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:b898d058564c6e8f16b8d652e13a9e6a522a70394c4337ef428e6ad430f91804`  
		Last Modified: Fri, 15 Dec 2017 17:21:15 GMT  
		Size: 200.5 MB (200539864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73655033400cbd3c9785ae0f5cfa85389c87b87fbc727a627e8921f8c7e5e278`  
		Last Modified: Fri, 05 Jan 2018 00:51:23 GMT  
		Size: 171.4 MB (171448026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23.0-stretch` - linux; 386

```console
$ docker pull rust@sha256:3c212bbd0df19dee588a2f60a05ca96db7c5fa4163fcd36d9536c6ce077ef553
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511429084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd26453ae35b0775b750a202b1aff88972467ae9946e50e527844a2f61cd849`
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
# Wed, 13 Dec 2017 14:50:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 16:37:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:11:28 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:8ea5318279c9f2c159ea30e29a11732815fc890ad4c36bd02c273984d19a6224`  
		Last Modified: Wed, 13 Dec 2017 15:02:14 GMT  
		Size: 218.2 MB (218187101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db2a56de0016046b36fe953a17bc7f35813b80fde80a6b5839293006ccb1e0`  
		Last Modified: Fri, 05 Jan 2018 05:31:12 GMT  
		Size: 180.2 MB (180156190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.23-jessie`

```console
$ docker pull rust@sha256:ebda1a950dfd49b3a81a26c408fa5d3b489ee1c762269778d1c5000b88040fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.23-jessie` - linux; amd64

```console
$ docker pull rust@sha256:e3bf7ac34b74167e585c0051ff31c1796ee6cd0de34f7865896fc6a51753f6b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.5 MB (436478181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b100402c3b158e162487b17df82aeef19abbbdd3d6e1ca2098fcca18dab3a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:49:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:49:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 07:49:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:50:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:41 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:23:30 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b491c575b06601bb07a2d88bfc3ace6c6005edc1b4d8da3ba6e37e04e9592d6`  
		Last Modified: Tue, 12 Dec 2017 08:00:34 GMT  
		Size: 19.3 MB (19266203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b313b08bab3b8bbcf0de4171a2a80a01e67fab094f272819b76a58705d21ab28`  
		Last Modified: Tue, 12 Dec 2017 08:01:02 GMT  
		Size: 43.3 MB (43253338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d6678c3f0e0c6e2b58b51ad100912b7c0e4dfedf98a1808417216fd5d948e5`  
		Last Modified: Tue, 12 Dec 2017 08:01:40 GMT  
		Size: 135.0 MB (134968174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dd223b09f7ea917286f36585be6d664242342970092b20c566ce39799eb2d8`  
		Last Modified: Thu, 04 Jan 2018 19:43:32 GMT  
		Size: 186.4 MB (186390769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23-jessie` - linux; arm variant v7

```console
$ docker pull rust@sha256:00c3bf85b3ffdc36fe337d904c0f9fd0f2bda45d7433efd767fc13775a363002
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.4 MB (395368827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed9280211bee90c7cf29b1a367a8ef3e9a241b1c2901be89053311d9c50fd4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 13:27:05 GMT
ADD file:aeb57f3a84dc1b93e1d38a80409a407df553344149d5070ed79b656865c90c54 in / 
# Tue, 12 Dec 2017 13:27:06 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:14:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:14:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 14:15:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:17:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:18:29 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:26:00 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:95e140a16c792899abc97cadee0138064dd21346fe51aa332ca4cbbd5563383c`  
		Last Modified: Tue, 12 Dec 2017 13:38:47 GMT  
		Size: 48.7 MB (48691755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237499cbbf2c5155fadc128c997700f0c5ec6355ba9704d0ec3f81c29640c9c4`  
		Last Modified: Tue, 12 Dec 2017 14:30:53 GMT  
		Size: 18.3 MB (18265038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f718f16c2f9a8213b99fcb49e72dad0036d1426f09c089f1e389b684f26520`  
		Last Modified: Tue, 12 Dec 2017 14:31:23 GMT  
		Size: 39.7 MB (39727713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affc0d5be2fb6b1dbb9d86ff0f533d88026215828cb4b1893257572ebf86f8d2`  
		Last Modified: Tue, 12 Dec 2017 14:32:10 GMT  
		Size: 114.1 MB (114057010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8af88c0d3aafa806ad2c595cce96fb2a7bddae9c3b74079ff185da9bbcd459`  
		Last Modified: Fri, 05 Jan 2018 16:28:26 GMT  
		Size: 174.6 MB (174627311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23-jessie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:df79b88460d9f7df06539a66dab1ef7e35a17645fbd8e258a9982f25c3aa3551
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397061702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795b0bd90a7734e1e4b207b3bb9870da0865fcf74e3c6ed492899ebcaba45092`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 18:24:58 GMT
ADD file:f0da52be154f821919dcbfb92afd89714053ae507038126715c96ac77a6768e1 in / 
# Tue, 12 Dec 2017 18:24:59 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 15:52:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 15:52:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 15:54:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:01:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:32:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:50:01 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:7e6d91e96b32c4999458c6c0cda42f920e41aab0cfbf3153f6e013b222bf084d`  
		Last Modified: Tue, 12 Dec 2017 18:39:54 GMT  
		Size: 49.9 MB (49926676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f2d61ff35851bad52cd6e85a1aa2c7b986069f0e062b7199ea07bc705f60cc`  
		Last Modified: Fri, 15 Dec 2017 17:15:45 GMT  
		Size: 18.7 MB (18739771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113d3a736bdb3c71bbdebc354892ca5b3e58753ed7a23231f8335c9ef0dc4a2`  
		Last Modified: Fri, 15 Dec 2017 17:16:09 GMT  
		Size: 41.0 MB (41021189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cf756b1b5f041ca4a78dc397a47f650ce6012584924a41c96fdf5da2edd2dc`  
		Last Modified: Fri, 15 Dec 2017 17:16:55 GMT  
		Size: 115.9 MB (115925986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1feb78ef2611564247fce161f72b48441e3a464f9924017cc96cd3392a76e16`  
		Last Modified: Fri, 05 Jan 2018 00:53:30 GMT  
		Size: 171.4 MB (171448080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23-jessie` - linux; 386

```console
$ docker pull rust@sha256:327631815fd6aff2bbdc6de73586f82a148d1f9439c24015b524bb7bc7bac08c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 MB (433592766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b111969f24678ebfcbb38c9bdca3bd9825860519dd54e8a73f47206c3d4b15`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 14:19:55 GMT
ADD file:235a40e05b677eb2ae7e7a3cc5cbb0cda242ff15dddb87cb8dc9bb0cd2d6aed8 in / 
# Tue, 12 Dec 2017 14:19:55 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 16:53:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 16:53:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 16:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 16:56:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 20:23:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:20:57 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d99577c7ee3d4d82987bedaeb10f3244ff7e19e41c5259bb8cac00568d1c4271`  
		Last Modified: Tue, 12 Dec 2017 14:46:26 GMT  
		Size: 52.8 MB (52777369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94aafa6d6f35f82e1fdc93cd4f7f6ab829f6297c8defaaa911dfb2de063bf3d`  
		Last Modified: Tue, 12 Dec 2017 17:27:39 GMT  
		Size: 21.6 MB (21596374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd19391b0ebd36e15e21cb3a6728c5950937634b9c81ecc7e3d1422b1dc25eb`  
		Last Modified: Tue, 12 Dec 2017 17:28:18 GMT  
		Size: 43.9 MB (43918299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8333879ca1894c745f67c724a7e4ad35542f5966a47bb050928910a944130ea0`  
		Last Modified: Tue, 12 Dec 2017 17:29:10 GMT  
		Size: 135.1 MB (135144789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d89f6a0e149d67f583d88c42593cf41d53d93a623aa6870162b8c32ec94ff`  
		Last Modified: Fri, 05 Jan 2018 05:43:12 GMT  
		Size: 180.2 MB (180155935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.23-stretch`

```console
$ docker pull rust@sha256:98b208cc6c5996bd3c4cf580a076e8b070d2916f243057dc6b7f9770c54bd58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.23-stretch` - linux; amd64

```console
$ docker pull rust@sha256:f087d993dce386920e0ebe72411b755b5827abc441581d9964dd39eeae6d52b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.1 MB (510064070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f381373aec8d0033cd25bdab8f641b4c847dc2f738432133620c33076b07ed`
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
# Tue, 12 Dec 2017 07:56:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:13:12 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:0f46f97746e4df5959e8c821ca69fdd6c0bedd611c1e0ab3b6970f7202b9bb10`  
		Last Modified: Tue, 12 Dec 2017 08:05:32 GMT  
		Size: 213.1 MB (213085177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3767d6ece93daba294352c76824377023d5b88fa8841d362ac4fcd5aa2f031`  
		Last Modified: Thu, 04 Jan 2018 19:34:05 GMT  
		Size: 186.4 MB (186391661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:4295abe2158b5f0648a51a9b5499642b7ff365b62afe0bce0f470871fe39f8a8
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.5 MB (470469897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab6533f9a6de2edeaf144f8af5d45e354191989de2af398b065ac7ddaa8a25`
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
# Tue, 12 Dec 2017 14:24:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:16:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:25:18 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:6b98be7e69ceba1d8ac982eeed4ed62c19e27b2ecff5a4e00df3e9e5add17b9c`  
		Last Modified: Tue, 12 Dec 2017 14:36:34 GMT  
		Size: 193.9 MB (193909280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2edc30150366daf2b75a4c16b463dfcca1946afee4aa8b9b2c668d14b87430`  
		Last Modified: Fri, 05 Jan 2018 16:27:02 GMT  
		Size: 174.6 MB (174627147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28398c3e11a206b5e83353c755a901ddc42252cd6fcf9d419b6ef2b2e2641764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477037975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539a3f74443cb8b611b6fb779294a77f508f464bbaebd21aa5d19801957ce784`
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
# Fri, 15 Dec 2017 16:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:31:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:48:42 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:b898d058564c6e8f16b8d652e13a9e6a522a70394c4337ef428e6ad430f91804`  
		Last Modified: Fri, 15 Dec 2017 17:21:15 GMT  
		Size: 200.5 MB (200539864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73655033400cbd3c9785ae0f5cfa85389c87b87fbc727a627e8921f8c7e5e278`  
		Last Modified: Fri, 05 Jan 2018 00:51:23 GMT  
		Size: 171.4 MB (171448026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.23-stretch` - linux; 386

```console
$ docker pull rust@sha256:3c212bbd0df19dee588a2f60a05ca96db7c5fa4163fcd36d9536c6ce077ef553
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511429084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd26453ae35b0775b750a202b1aff88972467ae9946e50e527844a2f61cd849`
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
# Wed, 13 Dec 2017 14:50:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 16:37:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:11:28 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:8ea5318279c9f2c159ea30e29a11732815fc890ad4c36bd02c273984d19a6224`  
		Last Modified: Wed, 13 Dec 2017 15:02:14 GMT  
		Size: 218.2 MB (218187101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db2a56de0016046b36fe953a17bc7f35813b80fde80a6b5839293006ccb1e0`  
		Last Modified: Fri, 05 Jan 2018 05:31:12 GMT  
		Size: 180.2 MB (180156190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1-jessie`

```console
$ docker pull rust@sha256:ebda1a950dfd49b3a81a26c408fa5d3b489ee1c762269778d1c5000b88040fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-jessie` - linux; amd64

```console
$ docker pull rust@sha256:e3bf7ac34b74167e585c0051ff31c1796ee6cd0de34f7865896fc6a51753f6b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.5 MB (436478181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b100402c3b158e162487b17df82aeef19abbbdd3d6e1ca2098fcca18dab3a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:49:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:49:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 07:49:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:50:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:41 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:23:30 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b491c575b06601bb07a2d88bfc3ace6c6005edc1b4d8da3ba6e37e04e9592d6`  
		Last Modified: Tue, 12 Dec 2017 08:00:34 GMT  
		Size: 19.3 MB (19266203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b313b08bab3b8bbcf0de4171a2a80a01e67fab094f272819b76a58705d21ab28`  
		Last Modified: Tue, 12 Dec 2017 08:01:02 GMT  
		Size: 43.3 MB (43253338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d6678c3f0e0c6e2b58b51ad100912b7c0e4dfedf98a1808417216fd5d948e5`  
		Last Modified: Tue, 12 Dec 2017 08:01:40 GMT  
		Size: 135.0 MB (134968174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dd223b09f7ea917286f36585be6d664242342970092b20c566ce39799eb2d8`  
		Last Modified: Thu, 04 Jan 2018 19:43:32 GMT  
		Size: 186.4 MB (186390769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-jessie` - linux; arm variant v7

```console
$ docker pull rust@sha256:00c3bf85b3ffdc36fe337d904c0f9fd0f2bda45d7433efd767fc13775a363002
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.4 MB (395368827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed9280211bee90c7cf29b1a367a8ef3e9a241b1c2901be89053311d9c50fd4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 13:27:05 GMT
ADD file:aeb57f3a84dc1b93e1d38a80409a407df553344149d5070ed79b656865c90c54 in / 
# Tue, 12 Dec 2017 13:27:06 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:14:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:14:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 14:15:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:17:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:18:29 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:26:00 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:95e140a16c792899abc97cadee0138064dd21346fe51aa332ca4cbbd5563383c`  
		Last Modified: Tue, 12 Dec 2017 13:38:47 GMT  
		Size: 48.7 MB (48691755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237499cbbf2c5155fadc128c997700f0c5ec6355ba9704d0ec3f81c29640c9c4`  
		Last Modified: Tue, 12 Dec 2017 14:30:53 GMT  
		Size: 18.3 MB (18265038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f718f16c2f9a8213b99fcb49e72dad0036d1426f09c089f1e389b684f26520`  
		Last Modified: Tue, 12 Dec 2017 14:31:23 GMT  
		Size: 39.7 MB (39727713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affc0d5be2fb6b1dbb9d86ff0f533d88026215828cb4b1893257572ebf86f8d2`  
		Last Modified: Tue, 12 Dec 2017 14:32:10 GMT  
		Size: 114.1 MB (114057010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8af88c0d3aafa806ad2c595cce96fb2a7bddae9c3b74079ff185da9bbcd459`  
		Last Modified: Fri, 05 Jan 2018 16:28:26 GMT  
		Size: 174.6 MB (174627311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-jessie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:df79b88460d9f7df06539a66dab1ef7e35a17645fbd8e258a9982f25c3aa3551
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397061702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795b0bd90a7734e1e4b207b3bb9870da0865fcf74e3c6ed492899ebcaba45092`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 18:24:58 GMT
ADD file:f0da52be154f821919dcbfb92afd89714053ae507038126715c96ac77a6768e1 in / 
# Tue, 12 Dec 2017 18:24:59 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 15:52:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 15:52:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 15:54:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:01:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:32:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:50:01 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:7e6d91e96b32c4999458c6c0cda42f920e41aab0cfbf3153f6e013b222bf084d`  
		Last Modified: Tue, 12 Dec 2017 18:39:54 GMT  
		Size: 49.9 MB (49926676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f2d61ff35851bad52cd6e85a1aa2c7b986069f0e062b7199ea07bc705f60cc`  
		Last Modified: Fri, 15 Dec 2017 17:15:45 GMT  
		Size: 18.7 MB (18739771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113d3a736bdb3c71bbdebc354892ca5b3e58753ed7a23231f8335c9ef0dc4a2`  
		Last Modified: Fri, 15 Dec 2017 17:16:09 GMT  
		Size: 41.0 MB (41021189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cf756b1b5f041ca4a78dc397a47f650ce6012584924a41c96fdf5da2edd2dc`  
		Last Modified: Fri, 15 Dec 2017 17:16:55 GMT  
		Size: 115.9 MB (115925986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1feb78ef2611564247fce161f72b48441e3a464f9924017cc96cd3392a76e16`  
		Last Modified: Fri, 05 Jan 2018 00:53:30 GMT  
		Size: 171.4 MB (171448080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-jessie` - linux; 386

```console
$ docker pull rust@sha256:327631815fd6aff2bbdc6de73586f82a148d1f9439c24015b524bb7bc7bac08c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 MB (433592766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b111969f24678ebfcbb38c9bdca3bd9825860519dd54e8a73f47206c3d4b15`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 14:19:55 GMT
ADD file:235a40e05b677eb2ae7e7a3cc5cbb0cda242ff15dddb87cb8dc9bb0cd2d6aed8 in / 
# Tue, 12 Dec 2017 14:19:55 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 16:53:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 16:53:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 16:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 16:56:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 20:23:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:20:57 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d99577c7ee3d4d82987bedaeb10f3244ff7e19e41c5259bb8cac00568d1c4271`  
		Last Modified: Tue, 12 Dec 2017 14:46:26 GMT  
		Size: 52.8 MB (52777369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94aafa6d6f35f82e1fdc93cd4f7f6ab829f6297c8defaaa911dfb2de063bf3d`  
		Last Modified: Tue, 12 Dec 2017 17:27:39 GMT  
		Size: 21.6 MB (21596374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd19391b0ebd36e15e21cb3a6728c5950937634b9c81ecc7e3d1422b1dc25eb`  
		Last Modified: Tue, 12 Dec 2017 17:28:18 GMT  
		Size: 43.9 MB (43918299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8333879ca1894c745f67c724a7e4ad35542f5966a47bb050928910a944130ea0`  
		Last Modified: Tue, 12 Dec 2017 17:29:10 GMT  
		Size: 135.1 MB (135144789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d89f6a0e149d67f583d88c42593cf41d53d93a623aa6870162b8c32ec94ff`  
		Last Modified: Fri, 05 Jan 2018 05:43:12 GMT  
		Size: 180.2 MB (180155935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1-stretch`

```console
$ docker pull rust@sha256:98b208cc6c5996bd3c4cf580a076e8b070d2916f243057dc6b7f9770c54bd58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-stretch` - linux; amd64

```console
$ docker pull rust@sha256:f087d993dce386920e0ebe72411b755b5827abc441581d9964dd39eeae6d52b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.1 MB (510064070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f381373aec8d0033cd25bdab8f641b4c847dc2f738432133620c33076b07ed`
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
# Tue, 12 Dec 2017 07:56:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:13:12 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:0f46f97746e4df5959e8c821ca69fdd6c0bedd611c1e0ab3b6970f7202b9bb10`  
		Last Modified: Tue, 12 Dec 2017 08:05:32 GMT  
		Size: 213.1 MB (213085177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3767d6ece93daba294352c76824377023d5b88fa8841d362ac4fcd5aa2f031`  
		Last Modified: Thu, 04 Jan 2018 19:34:05 GMT  
		Size: 186.4 MB (186391661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:4295abe2158b5f0648a51a9b5499642b7ff365b62afe0bce0f470871fe39f8a8
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.5 MB (470469897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab6533f9a6de2edeaf144f8af5d45e354191989de2af398b065ac7ddaa8a25`
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
# Tue, 12 Dec 2017 14:24:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:16:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:25:18 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:6b98be7e69ceba1d8ac982eeed4ed62c19e27b2ecff5a4e00df3e9e5add17b9c`  
		Last Modified: Tue, 12 Dec 2017 14:36:34 GMT  
		Size: 193.9 MB (193909280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2edc30150366daf2b75a4c16b463dfcca1946afee4aa8b9b2c668d14b87430`  
		Last Modified: Fri, 05 Jan 2018 16:27:02 GMT  
		Size: 174.6 MB (174627147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28398c3e11a206b5e83353c755a901ddc42252cd6fcf9d419b6ef2b2e2641764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477037975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539a3f74443cb8b611b6fb779294a77f508f464bbaebd21aa5d19801957ce784`
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
# Fri, 15 Dec 2017 16:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:31:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:48:42 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:b898d058564c6e8f16b8d652e13a9e6a522a70394c4337ef428e6ad430f91804`  
		Last Modified: Fri, 15 Dec 2017 17:21:15 GMT  
		Size: 200.5 MB (200539864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73655033400cbd3c9785ae0f5cfa85389c87b87fbc727a627e8921f8c7e5e278`  
		Last Modified: Fri, 05 Jan 2018 00:51:23 GMT  
		Size: 171.4 MB (171448026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-stretch` - linux; 386

```console
$ docker pull rust@sha256:3c212bbd0df19dee588a2f60a05ca96db7c5fa4163fcd36d9536c6ce077ef553
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511429084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd26453ae35b0775b750a202b1aff88972467ae9946e50e527844a2f61cd849`
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
# Wed, 13 Dec 2017 14:50:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 16:37:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:11:28 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:8ea5318279c9f2c159ea30e29a11732815fc890ad4c36bd02c273984d19a6224`  
		Last Modified: Wed, 13 Dec 2017 15:02:14 GMT  
		Size: 218.2 MB (218187101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db2a56de0016046b36fe953a17bc7f35813b80fde80a6b5839293006ccb1e0`  
		Last Modified: Fri, 05 Jan 2018 05:31:12 GMT  
		Size: 180.2 MB (180156190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:jessie`

```console
$ docker pull rust@sha256:ebda1a950dfd49b3a81a26c408fa5d3b489ee1c762269778d1c5000b88040fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:jessie` - linux; amd64

```console
$ docker pull rust@sha256:e3bf7ac34b74167e585c0051ff31c1796ee6cd0de34f7865896fc6a51753f6b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.5 MB (436478181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b100402c3b158e162487b17df82aeef19abbbdd3d6e1ca2098fcca18dab3a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:49:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:49:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 07:49:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:50:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:41 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:23:30 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b491c575b06601bb07a2d88bfc3ace6c6005edc1b4d8da3ba6e37e04e9592d6`  
		Last Modified: Tue, 12 Dec 2017 08:00:34 GMT  
		Size: 19.3 MB (19266203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b313b08bab3b8bbcf0de4171a2a80a01e67fab094f272819b76a58705d21ab28`  
		Last Modified: Tue, 12 Dec 2017 08:01:02 GMT  
		Size: 43.3 MB (43253338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d6678c3f0e0c6e2b58b51ad100912b7c0e4dfedf98a1808417216fd5d948e5`  
		Last Modified: Tue, 12 Dec 2017 08:01:40 GMT  
		Size: 135.0 MB (134968174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dd223b09f7ea917286f36585be6d664242342970092b20c566ce39799eb2d8`  
		Last Modified: Thu, 04 Jan 2018 19:43:32 GMT  
		Size: 186.4 MB (186390769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:jessie` - linux; arm variant v7

```console
$ docker pull rust@sha256:00c3bf85b3ffdc36fe337d904c0f9fd0f2bda45d7433efd767fc13775a363002
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.4 MB (395368827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed9280211bee90c7cf29b1a367a8ef3e9a241b1c2901be89053311d9c50fd4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 13:27:05 GMT
ADD file:aeb57f3a84dc1b93e1d38a80409a407df553344149d5070ed79b656865c90c54 in / 
# Tue, 12 Dec 2017 13:27:06 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:14:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:14:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 14:15:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:17:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:18:29 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:26:00 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:95e140a16c792899abc97cadee0138064dd21346fe51aa332ca4cbbd5563383c`  
		Last Modified: Tue, 12 Dec 2017 13:38:47 GMT  
		Size: 48.7 MB (48691755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237499cbbf2c5155fadc128c997700f0c5ec6355ba9704d0ec3f81c29640c9c4`  
		Last Modified: Tue, 12 Dec 2017 14:30:53 GMT  
		Size: 18.3 MB (18265038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f718f16c2f9a8213b99fcb49e72dad0036d1426f09c089f1e389b684f26520`  
		Last Modified: Tue, 12 Dec 2017 14:31:23 GMT  
		Size: 39.7 MB (39727713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affc0d5be2fb6b1dbb9d86ff0f533d88026215828cb4b1893257572ebf86f8d2`  
		Last Modified: Tue, 12 Dec 2017 14:32:10 GMT  
		Size: 114.1 MB (114057010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8af88c0d3aafa806ad2c595cce96fb2a7bddae9c3b74079ff185da9bbcd459`  
		Last Modified: Fri, 05 Jan 2018 16:28:26 GMT  
		Size: 174.6 MB (174627311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:jessie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:df79b88460d9f7df06539a66dab1ef7e35a17645fbd8e258a9982f25c3aa3551
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397061702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795b0bd90a7734e1e4b207b3bb9870da0865fcf74e3c6ed492899ebcaba45092`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 18:24:58 GMT
ADD file:f0da52be154f821919dcbfb92afd89714053ae507038126715c96ac77a6768e1 in / 
# Tue, 12 Dec 2017 18:24:59 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 15:52:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 15:52:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 15:54:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:01:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:32:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:50:01 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:7e6d91e96b32c4999458c6c0cda42f920e41aab0cfbf3153f6e013b222bf084d`  
		Last Modified: Tue, 12 Dec 2017 18:39:54 GMT  
		Size: 49.9 MB (49926676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f2d61ff35851bad52cd6e85a1aa2c7b986069f0e062b7199ea07bc705f60cc`  
		Last Modified: Fri, 15 Dec 2017 17:15:45 GMT  
		Size: 18.7 MB (18739771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113d3a736bdb3c71bbdebc354892ca5b3e58753ed7a23231f8335c9ef0dc4a2`  
		Last Modified: Fri, 15 Dec 2017 17:16:09 GMT  
		Size: 41.0 MB (41021189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cf756b1b5f041ca4a78dc397a47f650ce6012584924a41c96fdf5da2edd2dc`  
		Last Modified: Fri, 15 Dec 2017 17:16:55 GMT  
		Size: 115.9 MB (115925986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1feb78ef2611564247fce161f72b48441e3a464f9924017cc96cd3392a76e16`  
		Last Modified: Fri, 05 Jan 2018 00:53:30 GMT  
		Size: 171.4 MB (171448080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:jessie` - linux; 386

```console
$ docker pull rust@sha256:327631815fd6aff2bbdc6de73586f82a148d1f9439c24015b524bb7bc7bac08c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 MB (433592766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b111969f24678ebfcbb38c9bdca3bd9825860519dd54e8a73f47206c3d4b15`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 14:19:55 GMT
ADD file:235a40e05b677eb2ae7e7a3cc5cbb0cda242ff15dddb87cb8dc9bb0cd2d6aed8 in / 
# Tue, 12 Dec 2017 14:19:55 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 16:53:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 16:53:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 16:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 16:56:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 20:23:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:20:57 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d99577c7ee3d4d82987bedaeb10f3244ff7e19e41c5259bb8cac00568d1c4271`  
		Last Modified: Tue, 12 Dec 2017 14:46:26 GMT  
		Size: 52.8 MB (52777369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94aafa6d6f35f82e1fdc93cd4f7f6ab829f6297c8defaaa911dfb2de063bf3d`  
		Last Modified: Tue, 12 Dec 2017 17:27:39 GMT  
		Size: 21.6 MB (21596374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd19391b0ebd36e15e21cb3a6728c5950937634b9c81ecc7e3d1422b1dc25eb`  
		Last Modified: Tue, 12 Dec 2017 17:28:18 GMT  
		Size: 43.9 MB (43918299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8333879ca1894c745f67c724a7e4ad35542f5966a47bb050928910a944130ea0`  
		Last Modified: Tue, 12 Dec 2017 17:29:10 GMT  
		Size: 135.1 MB (135144789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d89f6a0e149d67f583d88c42593cf41d53d93a623aa6870162b8c32ec94ff`  
		Last Modified: Fri, 05 Jan 2018 05:43:12 GMT  
		Size: 180.2 MB (180155935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:latest`

```console
$ docker pull rust@sha256:98b208cc6c5996bd3c4cf580a076e8b070d2916f243057dc6b7f9770c54bd58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:latest` - linux; amd64

```console
$ docker pull rust@sha256:f087d993dce386920e0ebe72411b755b5827abc441581d9964dd39eeae6d52b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.1 MB (510064070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f381373aec8d0033cd25bdab8f641b4c847dc2f738432133620c33076b07ed`
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
# Tue, 12 Dec 2017 07:56:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:13:12 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:0f46f97746e4df5959e8c821ca69fdd6c0bedd611c1e0ab3b6970f7202b9bb10`  
		Last Modified: Tue, 12 Dec 2017 08:05:32 GMT  
		Size: 213.1 MB (213085177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3767d6ece93daba294352c76824377023d5b88fa8841d362ac4fcd5aa2f031`  
		Last Modified: Thu, 04 Jan 2018 19:34:05 GMT  
		Size: 186.4 MB (186391661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:4295abe2158b5f0648a51a9b5499642b7ff365b62afe0bce0f470871fe39f8a8
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.5 MB (470469897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab6533f9a6de2edeaf144f8af5d45e354191989de2af398b065ac7ddaa8a25`
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
# Tue, 12 Dec 2017 14:24:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:16:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:25:18 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:6b98be7e69ceba1d8ac982eeed4ed62c19e27b2ecff5a4e00df3e9e5add17b9c`  
		Last Modified: Tue, 12 Dec 2017 14:36:34 GMT  
		Size: 193.9 MB (193909280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2edc30150366daf2b75a4c16b463dfcca1946afee4aa8b9b2c668d14b87430`  
		Last Modified: Fri, 05 Jan 2018 16:27:02 GMT  
		Size: 174.6 MB (174627147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28398c3e11a206b5e83353c755a901ddc42252cd6fcf9d419b6ef2b2e2641764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477037975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539a3f74443cb8b611b6fb779294a77f508f464bbaebd21aa5d19801957ce784`
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
# Fri, 15 Dec 2017 16:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:31:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:48:42 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:b898d058564c6e8f16b8d652e13a9e6a522a70394c4337ef428e6ad430f91804`  
		Last Modified: Fri, 15 Dec 2017 17:21:15 GMT  
		Size: 200.5 MB (200539864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73655033400cbd3c9785ae0f5cfa85389c87b87fbc727a627e8921f8c7e5e278`  
		Last Modified: Fri, 05 Jan 2018 00:51:23 GMT  
		Size: 171.4 MB (171448026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:3c212bbd0df19dee588a2f60a05ca96db7c5fa4163fcd36d9536c6ce077ef553
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511429084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd26453ae35b0775b750a202b1aff88972467ae9946e50e527844a2f61cd849`
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
# Wed, 13 Dec 2017 14:50:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 16:37:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:11:28 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:8ea5318279c9f2c159ea30e29a11732815fc890ad4c36bd02c273984d19a6224`  
		Last Modified: Wed, 13 Dec 2017 15:02:14 GMT  
		Size: 218.2 MB (218187101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db2a56de0016046b36fe953a17bc7f35813b80fde80a6b5839293006ccb1e0`  
		Last Modified: Fri, 05 Jan 2018 05:31:12 GMT  
		Size: 180.2 MB (180156190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:stretch`

```console
$ docker pull rust@sha256:98b208cc6c5996bd3c4cf580a076e8b070d2916f243057dc6b7f9770c54bd58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:stretch` - linux; amd64

```console
$ docker pull rust@sha256:f087d993dce386920e0ebe72411b755b5827abc441581d9964dd39eeae6d52b1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.1 MB (510064070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f381373aec8d0033cd25bdab8f641b4c847dc2f738432133620c33076b07ed`
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
# Tue, 12 Dec 2017 07:56:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:15:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2018 19:13:12 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:0f46f97746e4df5959e8c821ca69fdd6c0bedd611c1e0ab3b6970f7202b9bb10`  
		Last Modified: Tue, 12 Dec 2017 08:05:32 GMT  
		Size: 213.1 MB (213085177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3767d6ece93daba294352c76824377023d5b88fa8841d362ac4fcd5aa2f031`  
		Last Modified: Thu, 04 Jan 2018 19:34:05 GMT  
		Size: 186.4 MB (186391661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:4295abe2158b5f0648a51a9b5499642b7ff365b62afe0bce0f470871fe39f8a8
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.5 MB (470469897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab6533f9a6de2edeaf144f8af5d45e354191989de2af398b065ac7ddaa8a25`
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
# Tue, 12 Dec 2017 14:24:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 17:16:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 16:25:18 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:6b98be7e69ceba1d8ac982eeed4ed62c19e27b2ecff5a4e00df3e9e5add17b9c`  
		Last Modified: Tue, 12 Dec 2017 14:36:34 GMT  
		Size: 193.9 MB (193909280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2edc30150366daf2b75a4c16b463dfcca1946afee4aa8b9b2c668d14b87430`  
		Last Modified: Fri, 05 Jan 2018 16:27:02 GMT  
		Size: 174.6 MB (174627147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28398c3e11a206b5e83353c755a901ddc42252cd6fcf9d419b6ef2b2e2641764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477037975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539a3f74443cb8b611b6fb779294a77f508f464bbaebd21aa5d19801957ce784`
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
# Fri, 15 Dec 2017 16:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 21:31:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 00:48:42 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:b898d058564c6e8f16b8d652e13a9e6a522a70394c4337ef428e6ad430f91804`  
		Last Modified: Fri, 15 Dec 2017 17:21:15 GMT  
		Size: 200.5 MB (200539864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73655033400cbd3c9785ae0f5cfa85389c87b87fbc727a627e8921f8c7e5e278`  
		Last Modified: Fri, 05 Jan 2018 00:51:23 GMT  
		Size: 171.4 MB (171448026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:stretch` - linux; 386

```console
$ docker pull rust@sha256:3c212bbd0df19dee588a2f60a05ca96db7c5fa4163fcd36d9536c6ce077ef553
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511429084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd26453ae35b0775b750a202b1aff88972467ae9946e50e527844a2f61cd849`
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
# Wed, 13 Dec 2017 14:50:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 16:37:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2018 05:11:28 GMT
RUN set -eux;         dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='4b7a67cd971d713e0caef48b5754190aca19192d1863927a005c3432512b12dc' ;; 		armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='622190c3f478a56563d45f6fbc1fab02d356b631c28a1beba2c3e4c68de3c14c' ;; 		arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='a39d7643cdced9ad70a9927bbb0a861b579884f94793881b771d3a0f92c0ddd8' ;; 		i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='9e921fce4a2cc1f04095be6d623effdead0aab1261472e6933da9e6030330b90' ;; 		*) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;; 	esac;         url="https://static.rust-lang.org/rustup/archive/1.9.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --default-toolchain 1.23.0;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
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
	-	`sha256:8ea5318279c9f2c159ea30e29a11732815fc890ad4c36bd02c273984d19a6224`  
		Last Modified: Wed, 13 Dec 2017 15:02:14 GMT  
		Size: 218.2 MB (218187101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db2a56de0016046b36fe953a17bc7f35813b80fde80a6b5839293006ccb1e0`  
		Last Modified: Fri, 05 Jan 2018 05:31:12 GMT  
		Size: 180.2 MB (180156190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
