####编译安装php5.4.45
------
> ./configure --prefix=/usr/local/php5445 --enable-fpm 
> 默认安装的模块  Core,ctype,date,dom,ereg，fileinfo,filter,hash,iconv,json,libxml,pcre,PDO,pdo_sqlite,Phar,posix，Reflection,session,SimpleXML,SPL,sqlite3,standard,tokenizer,xml,xmlreader,xmlwriter

-----

yum -y install libvpx-devel

`./configure --prefix=/usr/local/php5445 --enable-fpm --with-config-file-path=/usr/local/php5445/conf --with-config-file-scan-dir=/usr/local/php5445/conf.d --with-openssl --with-zlib --enable-bcmath --with-bz2 --enable-calendar --with-curl --with-curlwrappers --with-enchant --enable-exif --enable-ftp --with-gd --with-jpeg-dir --with-freetype-dir --with-t1lib --enable-gd-native-ttf --with-png-dir --with-xpm-dir --enable-gd-jis-conv --with-libdir=lib64 --with-gettext --with-gmp --with-mhash --with-imap --with-kerberos --with-imap-ssl --with-interbase --enable-mbstring --with-mcrypt --with-pdo-firebird --with-zlib-dir --enable-shmop --enable-soap --enable-sockets  --enable-wddx --with-xsl --enable-zip --enable-mysqlnd --enable-fast-install --with-onig --enable-sysvmsg --enable-sysvsem --enable-sysvshm --with-tidy --with-readline  --with-pdo-mysql=mysqlnd --enable-embedded-mysqli --with-mysqli=mysqlnd --with-mysql=mysqlnd --with-mssql --enable-dtrace --with-vpx-dir `




无效的 
--enable-zend-multibyte
--enable-sqlite-utf8

     
