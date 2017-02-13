# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define :openstack do |openstack|
    openstack.vm.box = "ubuntu/trusty64"
    openstack.vm.hostname = "openstack"
    openstack.vm.network :public_network
    openstack.vm.provider "virtualbox" do |vbox|
      vbox.customize ["modifyvm", :id, "--memory", "6442"]
      vbox.customize ["modifyvm", :id, "--name", "openstack"]
    end
    openstack.vm.provision :ansible do |ansible|
                      ansible.playbook = "task/main.yml"
  end
  end
end
