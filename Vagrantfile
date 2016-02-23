# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "alexwenzel/webdev"

  config.vm.network "private_network", ip: "192.168.10.11"
  config.vm.synced_folder "./www", "/var/www"

  config.ssh.insert_key=false

  config.vm.provider "virtualbox" do |vb|
  vb.memory = 2048
  end

end
