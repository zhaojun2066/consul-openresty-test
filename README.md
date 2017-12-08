###安装openresty

         wget http://luajit.org/download/LuaJIT-2.1.0-beta1.tar.gz
         tar -xvf LuaJIT-2.1.0-beta1.tar.gz
         cd LuaJIT-2.1.0-beta1
         make
         sudo make install

      下载：  http://openresty.org/cn/download.html
      安装依赖: apt-get install libreadline-dev libncurses5-dev libpcre3-dev \
        libssl-dev perl make build-essential
      安装: tar xzvf openresty-1.11.2.5.tar.gz
            cd openresty-1.11.2.5
            ./configure --prefix=/opt/openresty\
            --with-luajit

        make
        make install

        报错：
        error: ‘SSL_R_NO_CIPHERS_PASSED’ undeclared (first use in this function)
        || n == SSL_R_NO_CIPHERS_PASSED

      openssl 版本过高 ，手动制定openssl版本1.0.1
        ./configure   --with-openssl=/opt/openssl-1.0.1g