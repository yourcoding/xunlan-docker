#第一阶段：构建PHP应用
ARG PHP_FROM
FROM php:${PHP_FROM}

# 安装PHP所需的扩展
ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

#安装composer
COPY --from=composer /usr/bin/composer /usr/bin/composer

#安装工具包
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
&& apk update && apk upgrade \
&& apk add nginx supervisor tzdata unzip procps \
&& cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
&& echo "Shanghai/Asia" > /etc/timezone \
&& apk del tzdata \
&& chmod +x /usr/local/bin/install-php-extensions \
&& install-php-extensions bcmath exif gettext imagick intl mongodb mysqli pcntl pdo_mysql redis shmop soap sockets sysvsem xhprof xmlrpc xsl opcache zip xdebug \
&& mkdir -p /usr/local/php/bin && ln -sf /usr/local/bin/php /usr/local/php/bin/php \
&& mkdir -p /log \
&& chmod -R 777 /log \
&& ln -sf /dev/stdout /var/log/nginx/access.log \
&& ln -sf /dev/stderr /var/log/nginx/error.log \
&& rm -rf /var/cache/apk/*

#设置工作目录
WORKDIR /app

#启动
CMD ["supervisord", "-c", "/etc/supervisord.conf"]
