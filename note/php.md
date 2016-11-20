###编译安装php5.3.29
>最少项目： ./configure --prefix=/usr/local/php5329  --enable-fpm 
----- 
  默认安装模块  core,ctype,date,dom,ereg,fileinfo,filter,hash,iconv,json,libxml,pcre,pdo,pdo_sql_slite,phar,posix,Reflection,session,simplexml,spl,sqlite,sqlite3,standard,tokenizer,xml,xmlreader,xmlwriter.
  
> yum -y install bzip2-devel libcurl-devel enchant-devel t1lib-devel gmp-devel uw-imap-devel.x86_64  firebird-devel libicu-devel openldap-devel libmcrypt-devel unixODBC-devel  #postgresql-devel（7.4） net-snmp-devel freetds-devel
libtool-ltdl-devel libtidy-devel readline-devel recode-devel 

./configure --prefix=/usr/local/php5329 --enable-fpm --with-config-file-path=/usr/local/php5329/conf  --with-config-file-scan-dir=/usr/local/php5329/conf.d   --with-openssl  --with-zlib --enable-bcmath --with-bz2 --enable-calendar --with-curl --with-curlwrappers --with-enchant --enable-exif --enable-ftp --with-gd --with-jpeg-dir --with-freetype-dir --with-t1lib --enable-gd-native-ttf --with-png-dir --with-xpm-dir  --enable-gd-jis-conv --with-libdir=lib64 --with-gettext --with-gmp --with-mhash --with-imap --with-kerberos --with-imap-ssl --with-interbase --enable-mbstring  --with-mcrypt   --with-pdo-firebird  --with-zlib-dir --enable-shmop --enable-soap --enable-sockets  --enable-sqlite-utf8  --enable-wddx --with-xsl --enable-zip --enable-mysqlnd --enable-fast-install  --with-onig  --enable-sysvmsg --enable-sysvsem --enable-sysvshm --with-tidy --with-readline --enable-zend-multibyte --with-pdo-mysql=mysqlnd --enable-embedded-mysqli --with-mysqli=mysqlnd --with-mysql=mysqlnd --with-mssql


Notice: Following unknown configure options were used:

--with-solid
--with-ibm-db2
--with-empress
--with-empress-bcs
--with-birdstep
--with-unixODBC=/usr
--with-solid
--with-ibm-db2
--with-empress
--with-empress-bcs
--with-birdstep
--with-unixODBC=/usr



####添加命令行参数 ：
修改/etc/profile文件使其永久性生效，并对所有系统用户生效，在文件末尾加上如下两行代码
PATH=$PATH:/usr/local/webserver/php/bin:/usr/local/webserver/mysql/bin
export PATH

最后：执行 命令source /etc/profile或 执行点命令 ./profile使其修改生效，执行完可通过echo $PATH命令查看是否添加成功


####安装xcache
/usr/local/php5329/bin/phpize

./configure --enable-xcache --enable-xcache-constant --with-php-config=/usr/local/php5329/bin/php-config --enable-xcache-optimizer --enable-xcache-coverager --enable-xcache-assembler  --enable-xcache-disassembler --enable-xcache-encoder --enable-xcache-decoder --enable-xcache-test --enable-xcache-dprint --enable-shared=PKGS --enable-fast-install=PKGS 

####安装memcached扩展

yum -y install libevent-devel

./configure --enable-memcached  --enable-memcached-json   --enable-memcached-protocol --enable-shared=PKGS --enable-fast-install=PKGS --with-php-config=/usr/local/php5329/bin/php-config --with-libmemcached-dir





http://wowubuntu.com/markdown/index.html
