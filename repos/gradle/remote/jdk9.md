## `gradle:jdk9`

```console
$ docker pull gradle@sha256:489749f1982bed59a8d1e9e6fb58b906a2935e6241aea94e1b2248855cc2c058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gradle:jdk9` - linux; amd64

```console
$ docker pull gradle@sha256:e626d35b1ff87bb7ed596072cee8b0ffe8906af8e1132c71dc8bf0bed0c0f5be
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.1 MB (473101916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019de86ed64a19074a2d7fa55253d4e99e2421b6f59349fec96c1435363c2133`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 Dec 2017 01:43:09 GMT
ADD file:f4f0ede88e0b0edf8235b2a5ff46ab7d8de71d56720cb7dc3032bca0e1872695 in / 
# Tue, 12 Dec 2017 01:43:10 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:51:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:51:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 07:51:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:25:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:25:35 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:25:36 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:25:37 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:25:37 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 12 Dec 2017 15:25:38 GMT
ENV JAVA_VERSION=9.0.1+11
# Tue, 12 Dec 2017 15:25:38 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Tue, 12 Dec 2017 15:27:37 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:27:38 GMT
CMD ["jshell"]
# Tue, 12 Dec 2017 17:48:20 GMT
CMD ["gradle"]
# Tue, 12 Dec 2017 17:48:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 26 Jan 2018 18:20:43 GMT
ENV GRADLE_VERSION=4.5
# Fri, 26 Jan 2018 18:20:44 GMT
COPY file:e08b5c84a9d5a31f261ecabb5457633b5bf067646b5794580a81902b3318127f in /etc/ssl/certs/java/cacerts 
# Fri, 26 Jan 2018 18:20:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=03f2a43a314ff0fb843a85ef68078e06d181c4549c1e5fb983f289382b59b5e3
# Fri, 26 Jan 2018 18:20:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03f2a43a314ff0fb843a85ef68078e06d181c4549c1e5fb983f289382b59b5e3
RUN set -o errexit -o nounset 	&& echo "Downloading Gradle" 	&& wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip" 		&& echo "Checking download hash" 	&& echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check - 		&& echo "Installing Gradle" 	&& unzip gradle.zip 	&& rm gradle.zip 	&& mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/" 	&& ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle 		&& echo "Adding gradle user and group" 	&& groupadd --system --gid 1000 gradle 	&& useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle 	&& mkdir /home/gradle/.gradle 	&& chown --recursive gradle:gradle /home/gradle 		&& echo "Symlinking root Gradle cache to gradle Gradle cache" 	&& ln -s /home/gradle/.gradle /root/.gradle
# Fri, 26 Jan 2018 18:20:50 GMT
USER [gradle]
# Fri, 26 Jan 2018 18:20:50 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 26 Jan 2018 18:20:50 GMT
WORKDIR /home/gradle
# Fri, 26 Jan 2018 18:20:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03f2a43a314ff0fb843a85ef68078e06d181c4549c1e5fb983f289382b59b5e3
RUN set -o errexit -o nounset 	&& echo "Testing Gradle installation" 	&& gradle --version
```

-	Layers:
	-	`sha256:a8797cd0c76e8b1532d95708a0a38554c89e6fa0cdd856dbede8555225cdea00`  
		Last Modified: Tue, 12 Dec 2017 01:51:30 GMT  
		Size: 48.4 MB (48429060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdce62b256df9c745afac618b5a44d73531cede1a187586e73ed27bd7e1c508`  
		Last Modified: Tue, 12 Dec 2017 08:01:58 GMT  
		Size: 8.6 MB (8636787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c93763e33f35c3974631198e261ac389cb564d90b37f0443650ce34fee2dba2`  
		Last Modified: Tue, 12 Dec 2017 08:01:57 GMT  
		Size: 9.0 MB (8973876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbb22c778e9128dce650ba952241183b7375138fa397187b7967efef8221039`  
		Last Modified: Tue, 12 Dec 2017 08:02:29 GMT  
		Size: 48.6 MB (48567783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7d6f2e29096cc93e652b48e0f9cbe3c28587efeb67afb05a4a3c95bfd53cbd`  
		Last Modified: Tue, 12 Dec 2017 16:21:06 GMT  
		Size: 894.4 KB (894420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834793cb302ca7c856b57ded5f91611a4c74209cd8dd50fad662bf5479f954e0`  
		Last Modified: Tue, 12 Dec 2017 16:21:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35762e32445880df44cfe0452638ad5d1af2ca1b35e54ff612bc8de21a204f4`  
		Last Modified: Tue, 12 Dec 2017 16:21:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767ae54d85a98ebc04ac36a2f00fb89d040bb316d7e72258cb5ba95184a42bd8`  
		Last Modified: Tue, 12 Dec 2017 16:22:08 GMT  
		Size: 285.1 MB (285113816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc7dfb597058773f44e37d7a41534538cab3ce6e70564a65f1887e45fef2be6`  
		Last Modified: Fri, 26 Jan 2018 18:35:00 GMT  
		Size: 76.1 KB (76071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c0229d676f74670fe050cae4eec5e3bd85c78f94b991aec3f320da3c250987`  
		Last Modified: Fri, 26 Jan 2018 18:35:08 GMT  
		Size: 72.4 MB (72409586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db934def23a5160702e3436871cdb2b4da9e4ea3ad14d08cf0ebb9322d5382e`  
		Last Modified: Fri, 26 Jan 2018 18:35:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
