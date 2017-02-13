# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|  
  config.vm.define :open do |open|
    open.vm.box = "ubuntu/trusty64"
    open.vm.hostname = "openstack"
    open.vm.network :public_network, ip: "192.168.8.16" 
    open.vm.provider "virtualbox" do |vbox|
      vbox.customize ["modifyvm", :id, "--memory", "6442"]
      vbox.customize ["modifyvm", :id, "--name", "openstack"]
    end
  end
end
