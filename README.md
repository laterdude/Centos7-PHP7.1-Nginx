# Centos7-PHP7.1-Nginx
Installing PHP 7.1 on CentOS 7 with Nginx







####1. Install Nginx
`yum install nginx`



####2. Repo's for PHP 7.1
Unfortionally PHP7.1 is not available trough main stream repo's yet.

    $ yum install epel-release
    $ wget http://rpms.remirepo.net/enterprise/remi-release-7.rpm && rpm -Uvh remi-release-7.rpm


####2. Install PHP 7.1

    $ yum --enablerepo=remi-safe -y install php71

Version check: `php71 -v`


##### Some aditonal packages
    $ yum install php71-php-mcrypt php71-php-mcrypt php71-php-json php71-php-mbstring php71-php-xml php71-php-soap php71-php-xmlrpc php71-php-simplexml php71-php-curl php71-php-mysqlnd



####3. Install PHP-FPM
    
    $ yum --enablerepo=remi-safe -y install php71-php-fpm
    
#### Start & Set for boot
    $ systemctl start php71-php-fpm
    $ ystemctl status php71-php-fpm.service
    $ systemctl enable php71-php-fpm



### Configs?
In case you wonder, where the F**CK are my PHP / PHP FPM Config?
    
    /etc/opt/remi/php71/
    /etc/opt/remi/php71/php-fpm.d/www.conf


