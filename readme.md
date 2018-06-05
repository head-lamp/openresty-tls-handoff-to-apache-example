# rundown
when a request comes into your machine, nginx will be listening on :80 to redirect traffic over https
and will be listening on :443 to make the tls handshake

when a request comes in over https nginx will run some lua code that finds your 'server_name' and
then looks for some certs to make the tls handshake

after the handshake is complete it'll forward it to apache (or whatever is listening on :8080)

# installation
## (debian) instructions pulled from openresty website
### import openresty gpg key and add it to apt-key
```
$ wget -qO - https://openresty.org/package/pubkey.gpg | sudo apt-key add -
```

### for installing the add-apt-repository command
```
$ sudo apt-get -y install software-properties-common
```

### add the openresty official APT repository:
```
$ sudo add-apt-repository -y "deb http://openresty.org/package/debian $(lsb_release -sc) openresty"
```
### update apt index:
```
$ sudo apt-get update
```

### then install via
```
$ sudo apt-get install openresty
```

## fill out nginx.example.conf and cp it over to whereever your openresty/nginx/conf/nginx.conf is

## start openresty's ngninx server via
```
$ /path/to/ngninx -c /path/to/your/nginx.conf
```
