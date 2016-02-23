# Ubuntu Server 32bit 14.04 LTS with Apache, MySQl, PHP and several development tools installed.

This box is based on [ubuntu/trusty32](https://atlas.hashicorp.com/ubuntu/boxes/trusty32).

## Components

* apache
* mysql
* php 7
* sqlite
* vim
* git
* composer
* nodejs, npm
* cUrl
* xdebug

## Apache

Web Document Root: 

```
/var/www
```

## MySQL

User: 

```
root
```

Password:

```
root
```

## xDebug

Eanbled by trigger: 

```
XDEBUG_PROFILE=1
```

Output directory: 

```
/var/www/xdebug/
```

## Vagrantfile

    Vagrant.configure(2) do |config|
    
      config.vm.box = "alexwenzel/webdev"
    
      config.vm.network "private_network", ip: "192.168.10.10"
      config.vm.synced_folder "./www", "/var/www"
    
      config.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
      end
    
    end
