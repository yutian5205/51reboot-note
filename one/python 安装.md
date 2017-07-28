python 2.7 安装

    安装readline  不然退格上下左右键会乱码
	# yum install readline readline-devel
	
	# wget https://www.python.org/ftp/python/2.7.13/Python-2.7.13.tgz
	# tar xf Python-2.7.13.tgz 
	# ./configure --prefix=/usr/local/python
	# make && make install

	# mv /usr/bin/python /usr/bin/python_old
	# ln -s /usr/local/python/bin/python /usr/bin/python
	# vim /usr/bin/yum 
	#!/usr/bin/python_old
	
	安装pip
	
	# wget https://bootstrap.pypa.io/get-pip.py
	# wget https://bootstrap.pypa.io/ez_setup.py
	/usr/local/python/bin/python get-pip.py   
	/usr/local/python/bin/python ez_setup.py 

    安装pip get-pip.py 报错如下:

    zipimport.ZipImportError: can't decompress data; zlib not available

	解决：
    ./configure --prefix=/usr/local/python --with-zlib-dir=/usr/local/lib

    配置 python 源

    # vim ~/.pip/pip.conf

        [global]
        trusted-host=pypi.douban.com
        index-url = http://pypi.douban.com/simple

        [list]
        format = columns

