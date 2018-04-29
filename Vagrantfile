# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.username = "kai"
  config.ssh.password = "kai"
  config.vbguest.auto_update = false
  config.vm.box = "archlinux/archlinux"
  config.vm.network "private_network", ip: "192.168.10.25"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = "1"
  end

  config.vm.synced_folder "~/apps/src", "/home/kai/apps/src", owner: "kai", group: "kai"
end
