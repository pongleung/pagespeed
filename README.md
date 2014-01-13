Nginx Pagespeed App
======================
![](https://developers.google.com/speed/images/banner-carusel-pagespeed.png)

###Pagespeed app instalation and configuration for Nginx

Git Nginx Pagespeed App

    mkdir /etc/nginx/apps
    cd /etc/nginx/apps
    git clone https://github.com/Coozila/pagespeed
    
Update Nginx Pagespeed App

    cd /etc/nginx/apps/pagespeed
    git pull
    
Add Pagespeed app to your server block

    ## HTTP server.
    server {
    listen 80; # IPv4
    ## Replace the IPv6 address by your own address. The address below
    ## was stolen from the wikipedia page on IPv6.
    #listen [fe80::202:b3ff:fe1e:8330]:80 ipv6only=on;


    server_name test.yursite.com;


    ###########################################################################
    ## Nginx Pagespeed App 										
    ###########################################################################
    include apps/pagespeed/ngx_pagespeed.conf;


...
