# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.04"
  
  #config.vm.box_check_update = false

  config.vm.network "forwarded_port", guest: 8000, host: 8000
  
  config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y python-pip
     pip install pipenv
  SHELL
end
