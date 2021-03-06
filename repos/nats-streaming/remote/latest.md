## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:bedb1354eb262b0325a8c45da13344b63f93b7fec8fc2f0a695726826598e009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.2007; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:2157fbb4d253e16e46f45602b4fad8ce13eb9ee5d8cf0dbc78189baaf8cd9082
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3409973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32153a8463d2e0eb4032698a95cfb82ed6c29e9b7cb9f06244836bb5ee9d5c6d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 29 Jan 2018 22:55:37 GMT
COPY file:bf9b241b761aa6b1b2c125f21d42250015e1e234be8842e330a4fa129b48f570 in /nats-streaming-server 
# Mon, 29 Jan 2018 22:55:37 GMT
EXPOSE 4222/tcp 8222/tcp
# Mon, 29 Jan 2018 22:55:37 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 29 Jan 2018 22:55:38 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:025972d7004bac537ef4df931d06be2af2c8d86217b499e00054a88f4093855f`  
		Last Modified: Mon, 29 Jan 2018 22:55:56 GMT  
		Size: 3.4 MB (3409973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:920a5dbb8e60dfd5bf0092b01cd25e2bf5b0a36369e61fde95ba1c8b6baf7606
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2422cb256d3446eb2c562ad21070833ed4f7ea88b54f119eed57ee4cbfe5e88d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 30 Jan 2018 00:27:31 GMT
COPY file:77299fb658da8c200c8f6ec0e1e528411f3d97033c009d7e41ee3174c98bc2fd in /nats-streaming-server 
# Tue, 30 Jan 2018 00:27:32 GMT
EXPOSE 4222/tcp 8222/tcp
# Tue, 30 Jan 2018 00:27:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 30 Jan 2018 00:27:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ad775e7b077a28fa0be5ca43e491931638f5457237fe2239b07526353e71e010`  
		Last Modified: Tue, 30 Jan 2018 00:27:46 GMT  
		Size: 3.2 MB (3188288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:1d93af885422dcf5db30695764d947fac87b60e787d64a7fd4c9a0df933bbed4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3107555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a29b61023cde67641b9f650a1321a7eac1be26cbe9f0900442e868397606eb2`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 30 Jan 2018 01:27:58 GMT
COPY file:7ea57548ffaa3f165edb3c5ad4b961e2bade1713fc5be84a5d3d3a79e22ce878 in /nats-streaming-server 
# Tue, 30 Jan 2018 01:27:59 GMT
EXPOSE 4222/tcp 8222/tcp
# Tue, 30 Jan 2018 01:27:59 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 30 Jan 2018 01:28:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4648ebd89c1a06f19a6e4d36c6c8177ffce2c1ae499e109331286b9910861e03`  
		Last Modified: Tue, 30 Jan 2018 01:28:19 GMT  
		Size: 3.1 MB (3107555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.14393.2007; amd64

```console
$ docker pull nats-streaming@sha256:7495176713925a5eec6edd20e088775d3f958d6f42947061202673b7a2e1b5c4
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.5 MB (406505263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283940e7b86119b3df467ce004a2b7cef4b023d9966850d5f30a515bd9e822e0`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 13 Dec 2016 10:47:17 GMT
RUN Apply image 10.0.14393.0
# Thu, 04 Jan 2018 20:07:02 GMT
RUN Install update 10.0.14393.2007
# Thu, 04 Jan 2018 23:30:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 04 Jan 2018 23:30:27 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Mon, 29 Jan 2018 23:20:14 GMT
RUN cmd /S /C #(nop) COPY file:9971bf6318264cf9455380b7b27a366f48421824c236724959087374577a8d44 in nats-streaming-server.exe 
# Mon, 29 Jan 2018 23:20:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222/tcp 8222/tcp
# Mon, 29 Jan 2018 23:20:15 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bce2fbc256ea437a87dadac2f69aabd25bed4f56255549090056c1131fad0277`  
		Last Modified: Tue, 13 Dec 2016 10:47:17 GMT  
		Size: 252.7 MB (252691002 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764aee428c28f0935a6ded2a2730509373e1357648795b609b911dd46aa06257`  
		Last Modified: Thu, 04 Jan 2018 20:07:02 GMT  
		Size: 150.4 MB (150357748 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17dbcc3dc4bd52b77b681666085b3fcd9ee5fc59df7d486ba54e0867c1b24971`  
		Last Modified: Thu, 04 Jan 2018 23:30:50 GMT  
		Size: 939.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8743e28281d5bf7f7de45ffdd8357deae9ae6c82bcf382acbef032b82f36adc1`  
		Last Modified: Thu, 04 Jan 2018 23:30:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc00647abfe232a3729bba1bf87a2351f6854c7b9e725126464dc66764c144e0`  
		Last Modified: Mon, 29 Jan 2018 23:20:34 GMT  
		Size: 3.5 MB (3452514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ed2784fd83125db180334fbbcbf51eda4db8d1272e9b9166a920d422e19b55`  
		Last Modified: Mon, 29 Jan 2018 23:20:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10a1e754143a746fcc70fa29f48fac180d43544ca1ba776d73aacceb6d2f61e`  
		Last Modified: Mon, 29 Jan 2018 23:20:33 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
