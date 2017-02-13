# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define :open do |open|
    open.vm.box = "ubuntu/trusty64"
    open.vm.hostname = "openstack"
    open.vm.network :public_network
    open.vm.provider "virtualbox" do |vbox|
      vbox.customize ["modifyvm", :id, "--memory", "6442"]
      vbox.customize ["modifyvm", :id, "--name", "openstack"]
    end
    open.vm.provison :ansible do |ansible|
                      ansible.playbook = "main.yml"
  end
end
