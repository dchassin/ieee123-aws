# Installation
You need to install httpd and mysqld on your system before running these commands.
```
  host% cd /var/www/html
   (on a Mac use /Library/WebServer/Document instead of /var/www/html)
  host% git clone https://github.com/dchassin/ieee123-aws .
  host% mkdir output data
  host% cp config/default.php config/local.php
  host% chmod 777 output data
  host% git clone https://github.com/dchassin/gridlabd source
  host% cd source
  host% autoreconf -isf
  host% ./configure --enable-silent-rules --prefix=/usr/local --with-mysql 'CXXFLAGS=-w' 'CFLAGS=-w'
  host% make install
  host% service httpd restart
```

# Configuration

1. Using your browser open the URL http://localhost/
1. Configure your simulation by selecting the weather location and clicking [Save].
1. Click the [Restart] button to start the simulation.


