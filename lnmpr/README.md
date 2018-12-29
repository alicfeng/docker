No matter where I am, I will reply you immediately when I see the email.

My Email: echo "YUBzYW1lZ28uY29tCg==" | base64 -d



## `Nginx` + `PHP`+ `MySQL` + `Redis`

- 版本说明

  `Nginx` 👉1.15.3

  `MySQL`👉**5.7

  `PHP`👉7.2

  `Redis`👉4.0.12



___

- 扩展组件列表

|     名称      |     说明      |    日期    |
| :-----------: | :-----------: | :--------: |
| `wkhtmltopdf` | `html`转`pdf` | 2018-12-29 |
| `supervisor`  |   守护进程    | 2018-12-29 |
|               |               |            |



- `docker-compose`的`srv`结构

  ```shell
  srv
      ├── mysql
      │   └── config
      │       └── my.cnf
      ├── nginx
      │   ├── conf.d
      │   │   ├── api.yi-insurance.com.conf
      │   │   └── simple.conf.pl
      │   └── nginx.conf
      ├── php
      │   ├── php-fpm.conf
      │   ├── php.ini-development
      │   └── php.ini-production
      └── redis
          └── redis.conf
  ```


- 各服务详细配置说明

  1. 添加进程收入程序

     > 在如下目录添加单元配置
     >
     > `./srv/supervisor/supervisor.d/*.ini`

  2. `nginx`配置`映射域`

     > 在如下目录添加单元配置
     >
     > `./srv/nginx/conf.d/*.conf`



- 运行

  ```shell
  docker-compose up -d
  ```


- 留言

  关于`Nginx` +`PHP`的构建的流程是什么呢？[dockerfile](https://github.com/alicfeng/dockerfile/tree/master/nginx-php7)