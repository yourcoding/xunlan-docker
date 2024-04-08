```
xunlan-docker
├── README.md
├── .env
├── docker-compose.yml
├── buyer
│   ├── Dockerfile
│   ├── etc
│   │   ├── nginx
│   │   │   ├── http.d
│   │   │   │   ├── buyer.conf
│   │   │   │   └── default.conf.bak
│   │   │   ├── ssl
│   │   │   │   ├── nginx-selfsigned.crt
│   │   │   │   └── nginx-selfsigned.key
│   │   │   └── nginx.conf
│   │   ├── supervisor.d
│   │   │   ├── fpm.ini
│   │   │   └── nginx.ini
│   │   └── supervisord.conf    
│   ├── usr
│   │   └── local
│   │       └── etc
│   │          └── php
│   │               ├── conf.d
│   │               │    └── xdebug.ini
│   │               └── php.ini
│   ├── www
│   │   └── buyer                                                  #buyer - 项目代码
│   └── Dockerfile
├── common
│   ├── env
│   │   └── environment.php                                        #environment.php 需要替换
│   ├── geoip                                                      #geoip - IP库 - 需要覆盖
│   │   ├── GeoIP2-City.mmdb
│   │   └── GeoLite2-City.mmdb
│   └── yii2-vendor
├── mysql
│   ├── conf.d
│   ├── data
│   └── my.cnf
├── plugins
│   ├── Dockerfile
│   ├── etc
│   │   ├── nginx
│   │   │   ├── http.d
│   │   │   │   ├── buyer.conf
│   │   │   │   └── default.conf.bak
│   │   │   └── nginx.conf
│   │   ├── supervisor.d
│   │   │   ├── fpm.ini
│   │   │   └── nginx.ini
│   │   └── supervisord.conf    
│   ├── usr
│   │   └── local
│   │       └── etc
│   │          └── php
│   │               ├── conf.d
│   │               │    └── xdebug.ini
│   │               └── php.ini
│   ├── www
│   │   └── plugins                                                #plugins - 项目代码
│   └── Dockerfile
└── seller
    ├── Dockerfile
    ├── etc
    │   ├── nginx
    │   │   ├── http.d
    │   │   │   ├── buyer.conf
    │   │   │   └── default.conf.bak
    │   │   └── nginx.conf
    │   ├── supervisor.d
    │   │   ├── fpm.ini
    │   │   └── nginx.ini
    │   └── supervisord.conf    
    ├── usr
    │   └── local
    │       └── etc
    │          └── php
    │               ├── conf.d
    │               │    └── xdebug.ini
    │               └── php.ini
    ├── www
    │   └── s-backend                                              #s-backend - 项目代码
    └── Dockerfile
```
