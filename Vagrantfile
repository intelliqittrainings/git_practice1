# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
config.ssh.insert_key = false
config.vm.provider :virtualbox do |vb|
vb.customize ["modifyvm", :id, "--memory", "1024"]
 end

 # control
 config.vm.define "Jenkins" do |app|
 app.vm.hostname = "Jenkins"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "10.0.0.100"
 end
 
 
 # Load Balancer.
 config.vm.define "QA" do |app|
 app.vm.hostname = "QA"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "10.0.0.101"
 end
 
 # Application server 1.
 config.vm.define "Prod" do |app|
 app.vm.hostname = "Prod"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "10.0.0.102"
 end

 
 end
