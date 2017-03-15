# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "archlinux/archlinux"
  config.vbguest.auto_update = false
  config.vm.network "private_network", ip: "192.168.10.25"
  config.vm.synced_folder "~/apps/src", "/home/vagrant/apps/src"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = "1"
  end
end
