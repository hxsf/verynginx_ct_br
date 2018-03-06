
# [WIP]

# VeryNginx Dockerfile


A very powerful and friendly nginx based on lua-nginx-module [OpenResty](https://openresty.org) which provide WAF, Control Panel and Dashboards.

ImageLayers : [![](https://badge.imagelayers.io/hxsf/verynginx_ct_br:latest.svg)](https://imagelayers.io/?images=hxsf/verynginx_ct_br:latest)

This repository contains **Dockerfile** of [VeryNginx](https://github.com/alexazhou/VeryNginx)

Build with nginx_ct and nginx_brotli

## Informations


* Based on [Alpine Linux](http://www.alpinelinux.org/)  [alpine:3.7](https://hub.docker.com/r/_/alpine/)

## Installation


        docker pull hxsf/verynginx_ct_br
        cd ~
        git clone https://github.com/camilb/docker-verynginx.git


## Build


For example, if you need to install [Extra Modules](https://openresty.org), edit the Dockerfile and than build-it.

		cd ~/docker-verynginx
        docker build --rm -t hxsf/verynginx_ct_br .

# Usage


`Remove or modify conf.d/domain.conf and conf.d/domain-ssl.conf to match your needs :`


		cd ~/docker-verynginx
        docker run -d -v $PWD/conf.d:/etc/nginx/conf.d -p 80:80 -p 443:443 hxsf/verynginx_ct_br


###Test it:

	http://127.0.0.1/verynginx/index.html

	user: verynginx
	pass: verynginx
