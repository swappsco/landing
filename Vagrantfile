# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure(2) do |config|

  config.vm.box = "torchbox/wagtail-jessie64"
  config.vm.box_version = "~> 1.0"


  config.vm.network "forwarded_port", guest: 8000, host: 8000
  config.vm.network "private_network", ip: "192.168.33.105"

  config.vm.provision :shell, :path => "vagrant/provision.sh", :args => "app"

  config.ssh.forward_agent = true
end
