# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.disksize.size = '50GB'

  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.network "forwarded_port", guest: 27017, host: 5000 # MongoDB port.
  config.vm.network "forwarded_port", guest: 4000, host: 4000
  config.vm.network "forwarded_port", guest: 4001, host: 4001
  config.vm.network "forwarded_port", guest: 4002, host: 4002

  config.vm.provision "shell", path: "provision.sh"
end
