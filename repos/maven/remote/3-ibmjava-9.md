## `maven:3-ibmjava-9`

```console
$ docker pull maven@sha256:601f63fd01f2e8b763adf47546e47aef51a8a7f5bc80d9afd0b0c141fb25459d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-ibmjava-9` - linux; amd64

```console
$ docker pull maven@sha256:bce9389f87aa425619b148bd409a70bbecea5a975a63bb88acbf87fe703794f8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360159904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345204adf24930de1272ebf7a8e41db0def244fa40aff9d4b6a6438ad691224c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 15 Jan 2018 21:12:15 GMT
ADD file:affda766655e01cbd66cdf7485f581f22be61d93abadcc9fd22ed34c78069e18 in / 
# Mon, 15 Jan 2018 21:12:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 15 Jan 2018 21:12:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 15 Jan 2018 21:12:24 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 15 Jan 2018 21:12:34 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 15 Jan 2018 21:12:34 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2018 02:44:03 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 16 Jan 2018 02:44:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2018 03:11:29 GMT
ENV JAVA_VERSION=1.9.0_ea2
# Tue, 16 Jan 2018 03:12:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0fe3712b54a93695cf4948d9ae171bf5cef038c0e41b364b4e9eb7cb80a60688';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='5add39cc5ca56b97cf8ce71b9e1a15d19d36864aaed1e0296f50355ba3f34bd5';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3c0dda9f449a667d12fe5f59a1ec059a90a9dc483fd35eef5ff53dd8b096cdf5';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8d06af57d8236839f5c403c12dcf4c89e22dd91716a4d26b85c8d92f6d1e2e8b';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='6e823afa1df83e364381f827f4244bfe29b0ddd58ef0203eb60df9b8c0d123af';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(cat /tmp/index.yml | sed -n '/'${JAVA_VERSION}'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r');     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 16 Jan 2018 03:24:51 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2018 07:25:20 GMT
ARG MAVEN_VERSION=3.5.2
# Tue, 16 Jan 2018 07:25:21 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jan 2018 07:25:21 GMT
ARG SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff
# Tue, 16 Jan 2018 07:25:21 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries
# Tue, 16 Jan 2018 07:25:33 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries MAVEN_VERSION=3.5.2 SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 16 Jan 2018 07:25:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jan 2018 07:25:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jan 2018 07:39:02 GMT
COPY file:fb726a12bbbf8ff54c8d9fceef4fa3018c11a435bfa04ee5f73156c544907861 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 16 Jan 2018 07:39:03 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 16 Jan 2018 07:39:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jan 2018 07:39:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8f7c85c2269abaeba55439fe3a7e8935386d45a88da6166231fc947133c592a8`  
		Last Modified: Mon, 15 Jan 2018 14:45:34 GMT  
		Size: 42.8 MB (42842355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e72e494a6dd79fa00aaf2921eb571801c5ce9aee021bf5353f91f859aeee92f`  
		Last Modified: Mon, 15 Jan 2018 21:16:56 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3009ec50c8871f7a3f19c248194270a1a3aa28705934d619acbd96c663ce5c89`  
		Last Modified: Mon, 15 Jan 2018 21:16:56 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5ffccbec91702aeb063cb2f3987ca3661bd53dc9e4d8446261fe1c5b05de64`  
		Last Modified: Mon, 15 Jan 2018 21:16:57 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e872a2642ce1d63f3283e81bb6503579808c01e2bf63412ef87135ecb0f04746`  
		Last Modified: Mon, 15 Jan 2018 21:16:56 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df23f00c4a16647e27dd084c0150eabd8e6e242c99cfd0fbb754ca44a1e5e89a`  
		Last Modified: Tue, 16 Jan 2018 03:25:15 GMT  
		Size: 3.0 MB (3020970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0bbf2e77bd6023c1827e92e2ca91020cd31c1b29edf3054148a9b9c7c2b247`  
		Last Modified: Tue, 16 Jan 2018 03:30:00 GMT  
		Size: 271.6 MB (271633945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181d14ad253d0e3bc389b0ccc972d1cdd467ad807d822795d49df9990173222b`  
		Last Modified: Tue, 16 Jan 2018 07:40:20 GMT  
		Size: 42.7 MB (42659037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c758220a48cafa7e16057fc132d4f2c7a3c61a2611274f85e5eb8feda4ad48c`  
		Last Modified: Tue, 16 Jan 2018 07:41:59 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04aabb26b4755c2caa5038dd728cff4d50faf5d08e6269ca784e9e4d42ee5908`  
		Last Modified: Tue, 16 Jan 2018 07:41:59 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava-9` - linux; 386

```console
$ docker pull maven@sha256:2e6658220361fb9e5e20e36c2cc4b051eb76c8dedf3c831ff1397dcf0d78fc68
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341566821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9b87a5729875387d0314a29a8571fd21303f2d22ab9db67ff81ca6aa11c04f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jan 2018 05:11:31 GMT
ADD file:df10e819b9716197dc5e750b5584d563a145ec09d017b0234a56e459be7e0be8 in / 
# Tue, 16 Jan 2018 05:11:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 16 Jan 2018 05:11:32 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2018 05:11:33 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Tue, 16 Jan 2018 05:11:34 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 16 Jan 2018 05:11:34 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2018 06:11:10 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 16 Jan 2018 06:11:27 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2018 06:41:18 GMT
ENV JAVA_VERSION=1.9.0_ea2
# Tue, 16 Jan 2018 06:42:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0fe3712b54a93695cf4948d9ae171bf5cef038c0e41b364b4e9eb7cb80a60688';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='5add39cc5ca56b97cf8ce71b9e1a15d19d36864aaed1e0296f50355ba3f34bd5';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3c0dda9f449a667d12fe5f59a1ec059a90a9dc483fd35eef5ff53dd8b096cdf5';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8d06af57d8236839f5c403c12dcf4c89e22dd91716a4d26b85c8d92f6d1e2e8b';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='6e823afa1df83e364381f827f4244bfe29b0ddd58ef0203eb60df9b8c0d123af';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(cat /tmp/index.yml | sed -n '/'${JAVA_VERSION}'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r');     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 16 Jan 2018 06:51:36 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2018 10:32:27 GMT
ARG MAVEN_VERSION=3.5.2
# Tue, 16 Jan 2018 10:32:27 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jan 2018 10:32:28 GMT
ARG SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff
# Tue, 16 Jan 2018 10:32:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries
# Tue, 16 Jan 2018 10:32:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries MAVEN_VERSION=3.5.2 SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 16 Jan 2018 10:32:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jan 2018 10:32:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jan 2018 10:44:51 GMT
COPY file:fb726a12bbbf8ff54c8d9fceef4fa3018c11a435bfa04ee5f73156c544907861 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 16 Jan 2018 10:44:51 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 16 Jan 2018 10:44:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jan 2018 10:44:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e70160f4fa61966fa69c241da9f8107af2c8962479771c219db7b3436247ea36`  
		Last Modified: Mon, 15 Jan 2018 14:45:32 GMT  
		Size: 43.2 MB (43171534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942f28116bd0740eb362e3369ed6497c4f4adfa30b314868833d4bbaf146038a`  
		Last Modified: Tue, 16 Jan 2018 05:48:56 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8188f1ca382dc8eeb7d61f6079c3b693f70461bae546c48ce07b6035ff00f441`  
		Last Modified: Tue, 16 Jan 2018 05:48:56 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93d929ec938c6ef5d0321395d1d4ab1911e1711c9dd9775242d55d59c48167`  
		Last Modified: Tue, 16 Jan 2018 05:48:57 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23d87ded722d7e72329f4eef7debf29662f5ac33807c30fdfbe11e51023ba49`  
		Last Modified: Tue, 16 Jan 2018 05:48:58 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a0a290c9f9f059c886de291c21d98d561c02543e4c369c84e6f86f12edcd53`  
		Last Modified: Tue, 16 Jan 2018 07:00:04 GMT  
		Size: 2.9 MB (2877413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31a011a2cbc430291aa2eee57e4eb78757b263359a2c159425323b645b72e9b`  
		Last Modified: Tue, 16 Jan 2018 07:17:55 GMT  
		Size: 251.5 MB (251468483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177a821e346c4fb8e5aafd407ce04da453a2fa67e5dc82e9d679e28e63a4c26e`  
		Last Modified: Tue, 16 Jan 2018 11:25:11 GMT  
		Size: 44.0 MB (44045840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8ae23b8cd1bd6f380e4efb8d5fd34c380ac0dad81080e48ad6caacab37c459`  
		Last Modified: Tue, 16 Jan 2018 12:57:08 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f4852f92733b5e85441b566093260decbb4ce455c1ffbc251b19c14a915e7`  
		Last Modified: Tue, 16 Jan 2018 12:57:08 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava-9` - linux; ppc64le

```console
$ docker pull maven@sha256:e2e312553c0e4c80f54b8835295b4a057c7ce63221f1ff9d589a27aadcf7e082
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381742222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8ead3e2f428047fe0d7053e1c7dc7af47aa4487ce4b1800e6d4fcef4b32b9c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jan 2018 03:41:26 GMT
ADD file:428d6c211d39abb55269a867b80ea9baa241605171d1caf44af05b1a799c39f1 in / 
# Tue, 16 Jan 2018 03:41:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 16 Jan 2018 03:41:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2018 03:41:38 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Tue, 16 Jan 2018 03:41:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 16 Jan 2018 03:41:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2018 03:59:21 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 16 Jan 2018 03:59:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2018 04:06:07 GMT
ENV JAVA_VERSION=1.9.0_ea2
# Tue, 16 Jan 2018 04:11:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0fe3712b54a93695cf4948d9ae171bf5cef038c0e41b364b4e9eb7cb80a60688';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='5add39cc5ca56b97cf8ce71b9e1a15d19d36864aaed1e0296f50355ba3f34bd5';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3c0dda9f449a667d12fe5f59a1ec059a90a9dc483fd35eef5ff53dd8b096cdf5';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8d06af57d8236839f5c403c12dcf4c89e22dd91716a4d26b85c8d92f6d1e2e8b';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='6e823afa1df83e364381f827f4244bfe29b0ddd58ef0203eb60df9b8c0d123af';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(cat /tmp/index.yml | sed -n '/'${JAVA_VERSION}'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r');     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 16 Jan 2018 04:11:37 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2018 04:44:54 GMT
ARG MAVEN_VERSION=3.5.2
# Tue, 16 Jan 2018 04:44:56 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jan 2018 04:44:59 GMT
ARG SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff
# Tue, 16 Jan 2018 04:45:00 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries
# Tue, 16 Jan 2018 04:46:22 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries MAVEN_VERSION=3.5.2 SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 16 Jan 2018 04:46:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jan 2018 04:46:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jan 2018 04:47:16 GMT
COPY file:fb726a12bbbf8ff54c8d9fceef4fa3018c11a435bfa04ee5f73156c544907861 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 16 Jan 2018 04:47:19 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 16 Jan 2018 04:47:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jan 2018 04:47:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5d4a70e2296fafb78b369961815a69711acf05e939053c953bcba46e4db15f61`  
		Last Modified: Tue, 16 Jan 2018 03:43:42 GMT  
		Size: 45.3 MB (45272971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9c1ddbc9791ceb8d81c3a206b334f5e2c12a5980b51dcfcf81a9695fa67c33`  
		Last Modified: Tue, 16 Jan 2018 03:43:31 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d80d5b608f011672db438138da93404f73f97e2b67a8587cec29a7e55cdc9e`  
		Last Modified: Tue, 16 Jan 2018 03:43:31 GMT  
		Size: 649.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0061f3d18553c084eba4b2ab560a988b9e5071a3e2b3410665e32fd3351d76ed`  
		Last Modified: Tue, 16 Jan 2018 03:43:31 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35f843f0a152e7ff1e816674e1e670d611ef85f517888ded98998e4fb7439d8`  
		Last Modified: Tue, 16 Jan 2018 03:43:31 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2daea3e54b4f2db7ca92831ee255fecb8b4dec626fadd219566171178483479a`  
		Last Modified: Tue, 16 Jan 2018 04:11:57 GMT  
		Size: 2.9 MB (2878132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e555898e2c372264f52da0c1211049ce1a8cbf9a684c7333717a702410b6ab8`  
		Last Modified: Tue, 16 Jan 2018 04:14:25 GMT  
		Size: 292.0 MB (291957880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc81e40fd60631299418f761189948fa6ebd33744b0c92df7012d87ee635761`  
		Last Modified: Tue, 16 Jan 2018 04:48:15 GMT  
		Size: 41.6 MB (41629612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9f0c93e9750b73c5a03be47c1cac452fa5ba6b0ea002238bee7e4d5f24e411`  
		Last Modified: Tue, 16 Jan 2018 04:48:53 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc80f2986412233cfe6241f33f2ab12e25b5d9a4cfcd87a988b8ade8b7e225c6`  
		Last Modified: Tue, 16 Jan 2018 04:48:54 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava-9` - linux; s390x

```console
$ docker pull maven@sha256:b6922bf2f3e124709687f407358449568c1fc670ceb2a3e87fb4505bfb719d79
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.4 MB (359413462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0bc344edaba410b2468a57b3526a945430f724ce5771354adb906470d54dcf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jan 2018 14:15:42 GMT
ADD file:eb54587dae2601f015535da1845a3c71027dc1106e23926d56de34d894bab1a5 in / 
# Tue, 16 Jan 2018 14:15:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 16 Jan 2018 14:15:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2018 14:15:43 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Tue, 16 Jan 2018 14:15:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 16 Jan 2018 14:15:44 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2018 14:32:14 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 16 Jan 2018 14:32:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2018 14:35:13 GMT
ENV JAVA_VERSION=1.9.0_ea2
# Tue, 16 Jan 2018 14:36:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0fe3712b54a93695cf4948d9ae171bf5cef038c0e41b364b4e9eb7cb80a60688';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='5add39cc5ca56b97cf8ce71b9e1a15d19d36864aaed1e0296f50355ba3f34bd5';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3c0dda9f449a667d12fe5f59a1ec059a90a9dc483fd35eef5ff53dd8b096cdf5';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8d06af57d8236839f5c403c12dcf4c89e22dd91716a4d26b85c8d92f6d1e2e8b';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='6e823afa1df83e364381f827f4244bfe29b0ddd58ef0203eb60df9b8c0d123af';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(cat /tmp/index.yml | sed -n '/'${JAVA_VERSION}'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r');     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 16 Jan 2018 14:36:46 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2018 14:55:15 GMT
ARG MAVEN_VERSION=3.5.2
# Tue, 16 Jan 2018 14:55:15 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jan 2018 14:55:16 GMT
ARG SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff
# Tue, 16 Jan 2018 14:55:16 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries
# Tue, 16 Jan 2018 14:55:28 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries MAVEN_VERSION=3.5.2 SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 16 Jan 2018 14:55:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jan 2018 14:55:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jan 2018 14:56:09 GMT
COPY file:fb726a12bbbf8ff54c8d9fceef4fa3018c11a435bfa04ee5f73156c544907861 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 16 Jan 2018 14:56:09 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 16 Jan 2018 14:56:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jan 2018 14:56:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e1d2d19b3d250223ff28c57a8e4d47ab9e0792d49c5059d491a43ce072c3f6b2`  
		Last Modified: Tue, 16 Jan 2018 14:16:37 GMT  
		Size: 41.9 MB (41939461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6172ea68f95263549e8b4cc220767c6a7a01c1c2ebe0dbcea2146840674d36`  
		Last Modified: Tue, 16 Jan 2018 14:16:30 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eba87cef942a44e304c712541a1fd712a210840c26384df7de23a74f5ad0a80`  
		Last Modified: Tue, 16 Jan 2018 14:16:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e412096589b7a40ad29217023f54ef8f73ae230005b0b75ec9dbb162b358757`  
		Last Modified: Tue, 16 Jan 2018 14:16:30 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6662e74c0fb77d8af99843d5a75296c0778717195abaac2ef96f7d38ee8b83a4`  
		Last Modified: Tue, 16 Jan 2018 14:16:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce06ecdad2fdda84b4310c18409b3e15080853d191f871ae2b151073cc9bbb70`  
		Last Modified: Tue, 16 Jan 2018 14:37:05 GMT  
		Size: 2.8 MB (2765547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb20890a061371665e5f691b8b880200e25ea9d90ef3136665ffd0336b07b3d8`  
		Last Modified: Tue, 16 Jan 2018 14:38:37 GMT  
		Size: 274.7 MB (274684319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd3643b97537d023a616239093ad08b8720a14651a979ec4f99e967395e23c1`  
		Last Modified: Tue, 16 Jan 2018 14:56:45 GMT  
		Size: 40.0 MB (40020547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b4faa52f7f54a75cc3d9b42110e6b1f89fdbcefa0f6354d88991bced1e6c37`  
		Last Modified: Tue, 16 Jan 2018 14:57:04 GMT  
		Size: 740.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f480d9c1abbd02554eafffb2e9bb655301089457d92bf57f33fea1914edb20`  
		Last Modified: Tue, 16 Jan 2018 14:57:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
