#### 最小化安装php7.1.2

##### 默认安装的模块

> Core ctype  date dom fileinfo filter hash iconv json libxml pcre PDO pdo_sqlite Phar posix Reflection session SimpleXml SPL sqlite3 standard tokenizer xml xmlreader xmlwriter

```
# ./configure --prefix=/usr/local/php712\
 --enable-fpm\
 --with-fpm-acl\
 --enable-phpdbg\
 --enable-phpdbg-webhelper\
 --enable-gcov\
 --with-config-file-path=/usr/local/php712/conf\
 --with-config-file-scan-dir=/usr/local/php712/conf.d\
 --enable-dtrace\
 --with-openssl\
 --with-kerberos\
 --with-system-ciphers\
 --with-pcre-regex\
 --with-pcre-jit\
 --enable-bcmath\
 --with-bz2\
 --enable-calendar\
 --with-curl\
 --with-enchant\
 --enable-exif\
 --enable-ftp\
 --with-gd\
 --with-webp-dir\
 --with-jpeg-dir\
 --with-png-dir\
 --with-zlib-dir\
 --with-xpm-dir\
 --with-freetype-dir\
 --enable-gd-native-ttf\
 --enable-gd-jis-conv\
 --with-gettext\
 --with-gmp\
 --with-mhash\
 --with-imap\
 --enable-intl\
 --enable-mbstring\
 --with-mcrypt\
 --with-mysqli=mysqlnd\
 --enable-pcntl\
 --with-pdo-mysql\
 --with-readline\
 --enable-shmop\
 --with-snmp\
 --enable-soap\
 --enable-sockets\
 --enable-sysvmsg\
 --enable-sysvsem\
 --enable-sysvshm\
 --with-tidy\
 --enable-wddx\
 --with-xmlrpc\
 --enable-zip\
 --enable-mysqlnd\
 --with-xsl\
 --with-imap-ssl\



  --with-recode\
```
>      recode不能与imap同时编译




---
``` 
# yum -y install libxml2-devel zlib-devel libacl-devel lcov systemtap-sdt-devel openssl-devel libcurl-devel enchant-devel libwebp-devel libjpeg-turbo-devel gd-devel gmp-devel uw-imap-devel libicu-devel libmcrypt-devel readline-devel recode-devel net-snmp-devel libtidy-devel libxslt-devel bzip2-devel

ln -s /usr/lib64/libc-client.so /usr/lib/libc-client.so

