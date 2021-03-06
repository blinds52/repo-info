<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:10`](#odoo10)
-	[`odoo:10.0`](#odoo100)
-	[`odoo:11`](#odoo11)
-	[`odoo:11.0`](#odoo110)
-	[`odoo:9`](#odoo9)
-	[`odoo:9.0`](#odoo90)
-	[`odoo:latest`](#odoolatest)

## `odoo:10`

```console
$ docker pull odoo@sha256:f5b7d9cf33a31aa139093c13d167c4e3e06a1aaabf8a43899018069db98544fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:10` - linux; amd64

```console
$ docker pull odoo@sha256:95803cb838f57dbcf9b123f249b3a3625afdd26c59234a70c151e5df6e24c5a8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277466457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0626bf10b07070a940c0ecad5e57363d7723bc415fef21779878b65767655f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 05:17:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Dec 2017 05:18:54 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python-gevent             python-pip             python-renderpm             python-support             python-watchdog         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 12 Dec 2017 05:20:28 GMT
ENV ODOO_VERSION=10.0
# Mon, 22 Jan 2018 20:22:12 GMT
ENV ODOO_RELEASE=20180122
# Mon, 22 Jan 2018 20:23:32 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo '836f0fb94aee0d3771cf2188309f6079ee35f83e odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 22 Jan 2018 20:23:33 GMT
COPY file:33fddeba88e5214ff2c7cd05a02348dc417a5de70b767d6ff559e871ee6d046a in / 
# Mon, 22 Jan 2018 20:23:33 GMT
COPY file:18e3dbead2bc096fe44ef1cfaa2a6e8dc1b27daeeb1d281cfdd552b805f2e767 in /etc/odoo/ 
# Mon, 22 Jan 2018 20:23:34 GMT
RUN chown odoo /etc/odoo/odoo.conf
# Mon, 22 Jan 2018 20:23:35 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Mon, 22 Jan 2018 20:23:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jan 2018 20:23:35 GMT
EXPOSE 8069/tcp 8071/tcp
# Mon, 22 Jan 2018 20:23:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jan 2018 20:23:36 GMT
USER [odoo]
# Mon, 22 Jan 2018 20:23:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2018 20:23:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b641c2e41be91034a2d7c9bf3262b217cf2867d5ceec0f4a96cd5774cc1770d`  
		Last Modified: Tue, 12 Dec 2017 05:24:31 GMT  
		Size: 88.7 MB (88739172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2559ccfe4172f5237def535b201697895eb91e5a29cc172f2343dd62dc6c1b7`  
		Last Modified: Mon, 22 Jan 2018 21:01:08 GMT  
		Size: 136.1 MB (136125699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865830e7d589c44a719cac16c50ad91b95ff2ced21ffd121bdfc294394ab6545`  
		Last Modified: Mon, 22 Jan 2018 21:00:15 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869ee7bd694ec51d1fe0bb06dbe6dd9840575c08a1a3b03a35322b0b29ada9d`  
		Last Modified: Mon, 22 Jan 2018 21:00:15 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c763dc24570f4485a084f09ba05c5ec390ef13256f7b1f2b53b72c1940377f5`  
		Last Modified: Mon, 22 Jan 2018 21:00:15 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb37389dc143b5c30bceefd573d656928ea136d5a65f3c9e23480f72ca4688f`  
		Last Modified: Mon, 22 Jan 2018 21:00:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:10.0`

```console
$ docker pull odoo@sha256:f5b7d9cf33a31aa139093c13d167c4e3e06a1aaabf8a43899018069db98544fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:10.0` - linux; amd64

```console
$ docker pull odoo@sha256:95803cb838f57dbcf9b123f249b3a3625afdd26c59234a70c151e5df6e24c5a8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277466457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0626bf10b07070a940c0ecad5e57363d7723bc415fef21779878b65767655f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 05:17:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Dec 2017 05:18:54 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python-gevent             python-pip             python-renderpm             python-support             python-watchdog         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 12 Dec 2017 05:20:28 GMT
ENV ODOO_VERSION=10.0
# Mon, 22 Jan 2018 20:22:12 GMT
ENV ODOO_RELEASE=20180122
# Mon, 22 Jan 2018 20:23:32 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo '836f0fb94aee0d3771cf2188309f6079ee35f83e odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 22 Jan 2018 20:23:33 GMT
COPY file:33fddeba88e5214ff2c7cd05a02348dc417a5de70b767d6ff559e871ee6d046a in / 
# Mon, 22 Jan 2018 20:23:33 GMT
COPY file:18e3dbead2bc096fe44ef1cfaa2a6e8dc1b27daeeb1d281cfdd552b805f2e767 in /etc/odoo/ 
# Mon, 22 Jan 2018 20:23:34 GMT
RUN chown odoo /etc/odoo/odoo.conf
# Mon, 22 Jan 2018 20:23:35 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Mon, 22 Jan 2018 20:23:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jan 2018 20:23:35 GMT
EXPOSE 8069/tcp 8071/tcp
# Mon, 22 Jan 2018 20:23:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jan 2018 20:23:36 GMT
USER [odoo]
# Mon, 22 Jan 2018 20:23:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2018 20:23:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b641c2e41be91034a2d7c9bf3262b217cf2867d5ceec0f4a96cd5774cc1770d`  
		Last Modified: Tue, 12 Dec 2017 05:24:31 GMT  
		Size: 88.7 MB (88739172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2559ccfe4172f5237def535b201697895eb91e5a29cc172f2343dd62dc6c1b7`  
		Last Modified: Mon, 22 Jan 2018 21:01:08 GMT  
		Size: 136.1 MB (136125699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865830e7d589c44a719cac16c50ad91b95ff2ced21ffd121bdfc294394ab6545`  
		Last Modified: Mon, 22 Jan 2018 21:00:15 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869ee7bd694ec51d1fe0bb06dbe6dd9840575c08a1a3b03a35322b0b29ada9d`  
		Last Modified: Mon, 22 Jan 2018 21:00:15 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c763dc24570f4485a084f09ba05c5ec390ef13256f7b1f2b53b72c1940377f5`  
		Last Modified: Mon, 22 Jan 2018 21:00:15 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb37389dc143b5c30bceefd573d656928ea136d5a65f3c9e23480f72ca4688f`  
		Last Modified: Mon, 22 Jan 2018 21:00:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:11`

```console
$ docker pull odoo@sha256:5530f38649ed1872e571d8846bc7804d2338b96b12ad2c4a2f1b18ecccf46bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11` - linux; amd64

```console
$ docker pull odoo@sha256:616ef500c86a3708f63a53508de83746461243c7f41b5eb88910542bbff44c9e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.6 MB (414555886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb646b6039b301f4e813277e31cb9ff050be6a9a5f0cd6f8a7c5218d5b17573`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 05:22:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Dec 2017 05:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 05:22:37 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python3-pip             python3-setuptools             python3-renderpm             libssl1.0-dev             xz-utils         && curl -o wkhtmltox.tar.xz -SL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.4/wkhtmltox-0.12.4_linux-generic-amd64.tar.xz         && echo '3f923f425d345940089e44c1466f6408b9619562 wkhtmltox.tar.xz' | sha1sum -c -         && tar xvf wkhtmltox.tar.xz         && cp wkhtmltox/lib/* /usr/local/lib/         && cp wkhtmltox/bin/* /usr/local/bin/         && cp -r wkhtmltox/share/man/man1 /usr/local/share/man/
# Tue, 12 Dec 2017 05:22:37 GMT
ENV ODOO_VERSION=11.0
# Mon, 22 Jan 2018 20:34:09 GMT
ENV ODOO_RELEASE=20180122
# Mon, 22 Jan 2018 20:35:25 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo '56f61789bc655aaa2c014a3c5f63d80805408359 odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 22 Jan 2018 20:42:48 GMT
RUN pip3 install num2words xlwt
# Mon, 22 Jan 2018 20:47:03 GMT
COPY file:33fddeba88e5214ff2c7cd05a02348dc417a5de70b767d6ff559e871ee6d046a in / 
# Mon, 22 Jan 2018 20:47:03 GMT
COPY file:db43c8e34bfc1a07c1c22547437af17629fbadb6633084c02cbfc0bb6069c9fd in /etc/odoo/ 
# Mon, 22 Jan 2018 20:47:04 GMT
RUN chown odoo /etc/odoo/odoo.conf
# Mon, 22 Jan 2018 20:47:05 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Mon, 22 Jan 2018 20:47:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jan 2018 20:47:05 GMT
EXPOSE 8069/tcp 8071/tcp
# Mon, 22 Jan 2018 20:47:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jan 2018 20:47:05 GMT
USER [odoo]
# Mon, 22 Jan 2018 20:47:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2018 20:47:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70518ac76bc0293637ea81d1936563cca08dea6c643b5a8507e1c621c370fb8c`  
		Last Modified: Tue, 12 Dec 2017 05:35:39 GMT  
		Size: 221.4 MB (221395553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1996eb6b6c346ff369d6e942244ab1e4f343bf53ac89e6dcee30bab3fc1bd06`  
		Last Modified: Mon, 22 Jan 2018 21:02:41 GMT  
		Size: 147.6 MB (147574574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871c44a18b9bf235be76fd9b9c47059e12371ae629e74e51e16e0db6961e16bf`  
		Last Modified: Mon, 22 Jan 2018 21:01:52 GMT  
		Size: 462.3 KB (462294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6cf3b703ef17275a7d0f1ed818b807ce5b3d7078c5c728148486d76289188`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ab43b4cfbe9d15d10ba370edd49da035dfbcfc6f03ba73a4013ed5140d5de`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f04509397d1b5d0689c5193813b9d1abbf3867e00504710c39a5ccfe5cdc13`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb8d99001756065b84c61b3a754dc4e4611880211b2b7dd50d6978806e214fc`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:11.0`

```console
$ docker pull odoo@sha256:5530f38649ed1872e571d8846bc7804d2338b96b12ad2c4a2f1b18ecccf46bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11.0` - linux; amd64

```console
$ docker pull odoo@sha256:616ef500c86a3708f63a53508de83746461243c7f41b5eb88910542bbff44c9e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.6 MB (414555886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb646b6039b301f4e813277e31cb9ff050be6a9a5f0cd6f8a7c5218d5b17573`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 05:22:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Dec 2017 05:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 05:22:37 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python3-pip             python3-setuptools             python3-renderpm             libssl1.0-dev             xz-utils         && curl -o wkhtmltox.tar.xz -SL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.4/wkhtmltox-0.12.4_linux-generic-amd64.tar.xz         && echo '3f923f425d345940089e44c1466f6408b9619562 wkhtmltox.tar.xz' | sha1sum -c -         && tar xvf wkhtmltox.tar.xz         && cp wkhtmltox/lib/* /usr/local/lib/         && cp wkhtmltox/bin/* /usr/local/bin/         && cp -r wkhtmltox/share/man/man1 /usr/local/share/man/
# Tue, 12 Dec 2017 05:22:37 GMT
ENV ODOO_VERSION=11.0
# Mon, 22 Jan 2018 20:34:09 GMT
ENV ODOO_RELEASE=20180122
# Mon, 22 Jan 2018 20:35:25 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo '56f61789bc655aaa2c014a3c5f63d80805408359 odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 22 Jan 2018 20:42:48 GMT
RUN pip3 install num2words xlwt
# Mon, 22 Jan 2018 20:47:03 GMT
COPY file:33fddeba88e5214ff2c7cd05a02348dc417a5de70b767d6ff559e871ee6d046a in / 
# Mon, 22 Jan 2018 20:47:03 GMT
COPY file:db43c8e34bfc1a07c1c22547437af17629fbadb6633084c02cbfc0bb6069c9fd in /etc/odoo/ 
# Mon, 22 Jan 2018 20:47:04 GMT
RUN chown odoo /etc/odoo/odoo.conf
# Mon, 22 Jan 2018 20:47:05 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Mon, 22 Jan 2018 20:47:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jan 2018 20:47:05 GMT
EXPOSE 8069/tcp 8071/tcp
# Mon, 22 Jan 2018 20:47:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jan 2018 20:47:05 GMT
USER [odoo]
# Mon, 22 Jan 2018 20:47:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2018 20:47:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70518ac76bc0293637ea81d1936563cca08dea6c643b5a8507e1c621c370fb8c`  
		Last Modified: Tue, 12 Dec 2017 05:35:39 GMT  
		Size: 221.4 MB (221395553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1996eb6b6c346ff369d6e942244ab1e4f343bf53ac89e6dcee30bab3fc1bd06`  
		Last Modified: Mon, 22 Jan 2018 21:02:41 GMT  
		Size: 147.6 MB (147574574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871c44a18b9bf235be76fd9b9c47059e12371ae629e74e51e16e0db6961e16bf`  
		Last Modified: Mon, 22 Jan 2018 21:01:52 GMT  
		Size: 462.3 KB (462294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6cf3b703ef17275a7d0f1ed818b807ce5b3d7078c5c728148486d76289188`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ab43b4cfbe9d15d10ba370edd49da035dfbcfc6f03ba73a4013ed5140d5de`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f04509397d1b5d0689c5193813b9d1abbf3867e00504710c39a5ccfe5cdc13`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb8d99001756065b84c61b3a754dc4e4611880211b2b7dd50d6978806e214fc`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:9`

```console
$ docker pull odoo@sha256:577c43fc81e060e22db28f0d18d93ed3d92693a1029b345f49f59a5cf64af3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:9` - linux; amd64

```console
$ docker pull odoo@sha256:f8862f5d460c5ed6435239963a09888da54e211befe3d93eb0c06a17a5ec7df4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289907796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbf496a93c12e1dd1f5b9a75ff63191c64e8e4399b37737e4437749f1aa31a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["openerp-server"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 05:17:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Dec 2017 05:18:54 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python-gevent             python-pip             python-renderpm             python-support             python-watchdog         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 12 Dec 2017 05:18:56 GMT
ENV ODOO_VERSION=9.0
# Mon, 22 Jan 2018 20:07:56 GMT
ENV ODOO_RELEASE=20180122
# Mon, 22 Jan 2018 20:09:45 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}c.${ODOO_RELEASE}_all.deb         && echo 'a623d188d48f08ce8bb8898355eccc5e5e7e5b04 odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 22 Jan 2018 20:09:46 GMT
COPY file:b514c2e8f66799bc707e194d35e0ef442ee72b46668e42cdfee105b6445d7eb0 in / 
# Mon, 22 Jan 2018 20:09:47 GMT
COPY file:5bf1f863cb98f8aeeac8f1a8430f1af56358cee4a6e5ade3b2c00fb3fc8d4162 in /etc/odoo/ 
# Mon, 22 Jan 2018 20:09:47 GMT
RUN chown odoo /etc/odoo/openerp-server.conf
# Mon, 22 Jan 2018 20:09:48 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Mon, 22 Jan 2018 20:09:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jan 2018 20:09:48 GMT
EXPOSE 8069/tcp 8071/tcp
# Mon, 22 Jan 2018 20:09:49 GMT
ENV OPENERP_SERVER=/etc/odoo/openerp-server.conf
# Mon, 22 Jan 2018 20:09:49 GMT
USER [odoo]
# Mon, 22 Jan 2018 20:09:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2018 20:09:49 GMT
CMD ["openerp-server"]
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b641c2e41be91034a2d7c9bf3262b217cf2867d5ceec0f4a96cd5774cc1770d`  
		Last Modified: Tue, 12 Dec 2017 05:24:31 GMT  
		Size: 88.7 MB (88739172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636846e9bc6a8b29fa1df08b8d4e4c119e0cbbbc91c8f4bd50c61181cefc5ea0`  
		Last Modified: Mon, 22 Jan 2018 20:48:17 GMT  
		Size: 148.6 MB (148567009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6409b2ce4c1be5f8b9bbb2e76bc720f270cc8242a7f9c80ebf6d863f39fb9586`  
		Last Modified: Mon, 22 Jan 2018 20:47:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c2a99832d811984a24c32bcb4491d4c7030af05821fa4387044726b918c9e2`  
		Last Modified: Mon, 22 Jan 2018 20:47:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ced77716650e8d390910c7970feae6327d77a367eba031e71081d83ef252a5`  
		Last Modified: Mon, 22 Jan 2018 20:47:25 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df82fbdd2a1cc690e52352947b092142dad44aa4b3b72954edee0033a4473837`  
		Last Modified: Mon, 22 Jan 2018 20:47:25 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:9.0`

```console
$ docker pull odoo@sha256:577c43fc81e060e22db28f0d18d93ed3d92693a1029b345f49f59a5cf64af3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:9.0` - linux; amd64

```console
$ docker pull odoo@sha256:f8862f5d460c5ed6435239963a09888da54e211befe3d93eb0c06a17a5ec7df4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289907796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbf496a93c12e1dd1f5b9a75ff63191c64e8e4399b37737e4437749f1aa31a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["openerp-server"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 05:17:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Dec 2017 05:18:54 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python-gevent             python-pip             python-renderpm             python-support             python-watchdog         && curl -o wkhtmltox.deb -SL http://nightly.odoo.com/extra/wkhtmltox-0.12.1.2_linux-jessie-amd64.deb         && echo '40e8b906de658a2221b15e4e8cd82565a47d7ee8 wkhtmltox.deb' | sha1sum -c -         && dpkg --force-depends -i wkhtmltox.deb         && apt-get -y install -f --no-install-recommends         && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false npm         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb         && pip install psycogreen==1.0
# Tue, 12 Dec 2017 05:18:56 GMT
ENV ODOO_VERSION=9.0
# Mon, 22 Jan 2018 20:07:56 GMT
ENV ODOO_RELEASE=20180122
# Mon, 22 Jan 2018 20:09:45 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}c.${ODOO_RELEASE}_all.deb         && echo 'a623d188d48f08ce8bb8898355eccc5e5e7e5b04 odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 22 Jan 2018 20:09:46 GMT
COPY file:b514c2e8f66799bc707e194d35e0ef442ee72b46668e42cdfee105b6445d7eb0 in / 
# Mon, 22 Jan 2018 20:09:47 GMT
COPY file:5bf1f863cb98f8aeeac8f1a8430f1af56358cee4a6e5ade3b2c00fb3fc8d4162 in /etc/odoo/ 
# Mon, 22 Jan 2018 20:09:47 GMT
RUN chown odoo /etc/odoo/openerp-server.conf
# Mon, 22 Jan 2018 20:09:48 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Mon, 22 Jan 2018 20:09:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jan 2018 20:09:48 GMT
EXPOSE 8069/tcp 8071/tcp
# Mon, 22 Jan 2018 20:09:49 GMT
ENV OPENERP_SERVER=/etc/odoo/openerp-server.conf
# Mon, 22 Jan 2018 20:09:49 GMT
USER [odoo]
# Mon, 22 Jan 2018 20:09:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2018 20:09:49 GMT
CMD ["openerp-server"]
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b641c2e41be91034a2d7c9bf3262b217cf2867d5ceec0f4a96cd5774cc1770d`  
		Last Modified: Tue, 12 Dec 2017 05:24:31 GMT  
		Size: 88.7 MB (88739172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636846e9bc6a8b29fa1df08b8d4e4c119e0cbbbc91c8f4bd50c61181cefc5ea0`  
		Last Modified: Mon, 22 Jan 2018 20:48:17 GMT  
		Size: 148.6 MB (148567009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6409b2ce4c1be5f8b9bbb2e76bc720f270cc8242a7f9c80ebf6d863f39fb9586`  
		Last Modified: Mon, 22 Jan 2018 20:47:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c2a99832d811984a24c32bcb4491d4c7030af05821fa4387044726b918c9e2`  
		Last Modified: Mon, 22 Jan 2018 20:47:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ced77716650e8d390910c7970feae6327d77a367eba031e71081d83ef252a5`  
		Last Modified: Mon, 22 Jan 2018 20:47:25 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df82fbdd2a1cc690e52352947b092142dad44aa4b3b72954edee0033a4473837`  
		Last Modified: Mon, 22 Jan 2018 20:47:25 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:5530f38649ed1872e571d8846bc7804d2338b96b12ad2c4a2f1b18ecccf46bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:616ef500c86a3708f63a53508de83746461243c7f41b5eb88910542bbff44c9e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.6 MB (414555886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb646b6039b301f4e813277e31cb9ff050be6a9a5f0cd6f8a7c5218d5b17573`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 05:22:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Dec 2017 05:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 05:22:37 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             node-less             python3-pip             python3-setuptools             python3-renderpm             libssl1.0-dev             xz-utils         && curl -o wkhtmltox.tar.xz -SL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.4/wkhtmltox-0.12.4_linux-generic-amd64.tar.xz         && echo '3f923f425d345940089e44c1466f6408b9619562 wkhtmltox.tar.xz' | sha1sum -c -         && tar xvf wkhtmltox.tar.xz         && cp wkhtmltox/lib/* /usr/local/lib/         && cp wkhtmltox/bin/* /usr/local/bin/         && cp -r wkhtmltox/share/man/man1 /usr/local/share/man/
# Tue, 12 Dec 2017 05:22:37 GMT
ENV ODOO_VERSION=11.0
# Mon, 22 Jan 2018 20:34:09 GMT
ENV ODOO_RELEASE=20180122
# Mon, 22 Jan 2018 20:35:25 GMT
RUN set -x;         curl -o odoo.deb -SL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo '56f61789bc655aaa2c014a3c5f63d80805408359 odoo.deb' | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 22 Jan 2018 20:42:48 GMT
RUN pip3 install num2words xlwt
# Mon, 22 Jan 2018 20:47:03 GMT
COPY file:33fddeba88e5214ff2c7cd05a02348dc417a5de70b767d6ff559e871ee6d046a in / 
# Mon, 22 Jan 2018 20:47:03 GMT
COPY file:db43c8e34bfc1a07c1c22547437af17629fbadb6633084c02cbfc0bb6069c9fd in /etc/odoo/ 
# Mon, 22 Jan 2018 20:47:04 GMT
RUN chown odoo /etc/odoo/odoo.conf
# Mon, 22 Jan 2018 20:47:05 GMT
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Mon, 22 Jan 2018 20:47:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jan 2018 20:47:05 GMT
EXPOSE 8069/tcp 8071/tcp
# Mon, 22 Jan 2018 20:47:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jan 2018 20:47:05 GMT
USER [odoo]
# Mon, 22 Jan 2018 20:47:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2018 20:47:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70518ac76bc0293637ea81d1936563cca08dea6c643b5a8507e1c621c370fb8c`  
		Last Modified: Tue, 12 Dec 2017 05:35:39 GMT  
		Size: 221.4 MB (221395553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1996eb6b6c346ff369d6e942244ab1e4f343bf53ac89e6dcee30bab3fc1bd06`  
		Last Modified: Mon, 22 Jan 2018 21:02:41 GMT  
		Size: 147.6 MB (147574574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871c44a18b9bf235be76fd9b9c47059e12371ae629e74e51e16e0db6961e16bf`  
		Last Modified: Mon, 22 Jan 2018 21:01:52 GMT  
		Size: 462.3 KB (462294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6cf3b703ef17275a7d0f1ed818b807ce5b3d7078c5c728148486d76289188`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ab43b4cfbe9d15d10ba370edd49da035dfbcfc6f03ba73a4013ed5140d5de`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f04509397d1b5d0689c5193813b9d1abbf3867e00504710c39a5ccfe5cdc13`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb8d99001756065b84c61b3a754dc4e4611880211b2b7dd50d6978806e214fc`  
		Last Modified: Mon, 22 Jan 2018 21:01:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
