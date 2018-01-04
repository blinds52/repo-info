## `openjdk:6-jdk-wheezy`

```console
$ docker pull openjdk@sha256:d195707b22cc64d027930857a0f28199d64c4d567151afbc031d86c0f8d636aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:6-jdk-wheezy` - linux; amd64

```console
$ docker pull openjdk@sha256:a7e7fe147d1295b6b9a55ec7cc89a80cf630950bffe71bc89b25930e34494fcb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189743075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c387b3746aaa795dcbfccad955398c09aa947baf0ecf6312aa851638a585dc9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 01:46:04 GMT
ADD file:281b987b09ac9b71793de5201331461636a08ec23af27a9e11a14484018993dd in / 
# Tue, 12 Dec 2017 01:46:04 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:56:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:56:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 07:57:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:00:26 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:00:27 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:00:28 GMT
RUN ln -svT "/usr/lib/jvm/java-6-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:00:29 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 12 Dec 2017 15:00:29 GMT
ENV JAVA_VERSION=6b38
# Tue, 12 Dec 2017 15:00:29 GMT
ENV JAVA_DEBIAN_VERSION=6b38-1.13.10-1~deb7u1
# Tue, 12 Dec 2017 15:01:24 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-6-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:762ae076e9a326e4eac3b3db9e3afe4b6dc930ec52dbb2aa27a300d1323a52b6`  
		Last Modified: Tue, 12 Dec 2017 01:59:44 GMT  
		Size: 38.1 MB (38109825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23de19d3f13a2be7ebc7920f3ba4c5b85177a11b50a1ade92d360c09aa349bf1`  
		Last Modified: Tue, 12 Dec 2017 08:06:02 GMT  
		Size: 7.0 MB (6950248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb3e44109931c7e35ceafc97c97e76d8f382673240ce180d61297082aa09a2`  
		Last Modified: Tue, 12 Dec 2017 08:06:29 GMT  
		Size: 38.0 MB (37961407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561c9ce93549a92fa3ba24fe98495abc1790218162d74f94d42284074d2bf43a`  
		Last Modified: Tue, 12 Dec 2017 15:44:26 GMT  
		Size: 616.6 KB (616639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f981f6dc4a262147ce89392b666e6c82590e7d3f4b1edc04a63a437ea7a6a9`  
		Last Modified: Tue, 12 Dec 2017 15:44:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f88a3742fa40e192be06c3a01022c399999375d6b5139d2ebed1b46ddda934a`  
		Last Modified: Tue, 12 Dec 2017 15:44:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2901d2c9cd4faf7bd7fe29bfa800bcf02fcb68d901e220109a264cdde703d7c0`  
		Last Modified: Tue, 12 Dec 2017 15:44:47 GMT  
		Size: 106.1 MB (106104578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip