#installation
##(debian) instructions pulled from openresty website
###import openresty gpg key and add it to apt-key
```
$ wget -qO - https://openresty.org/package/pubkey.gpg | sudo apt-key add -
```

###for installing the add-apt-repository command
```
$ sudo apt-get -y install software-properties-common
```

###add the openresty official APT repository:
```
$ sudo add-apt-repository -y "deb http://openresty.org/package/debian $(lsb_release -sc) openresty"
```
###update apt index:
```
$ sudo apt-get update
```

###then install via
```
$ sudo apt-get install openresty
```

##fill out nginx.example.conf and cp it over

##start openresty's ngninx server via
```
$ /path/to/ngninx -c /path/to/your/nginx.conf
```
