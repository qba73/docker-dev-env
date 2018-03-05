# -*- mode: ruby -*-
# vi: set ft=ruby :

BOX_IMAGE = "centos/7"
NUMBER_OF_NODES = 2

Vagrant.configure("2") do |config|
  config.vm.define "master" do |master|
    master.vm.box = BOX_IMAGE
    master.vm.hostname = "master"
    master.vm.network :private_network, ip: "10.0.0.10"
  end

  (1..NUMBER_OF_NODES).each do |n|
    config.vm.define "node#{n}" do |node|
      node.vm.box = BOX_IMAGE
      node.vm.hostname = "node#{i}"
      node.vm.network :private_network, ip: "10.0.0.#{n + 10}"
    end
  end
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end

  # config.vm.provision "shell", inline: <<-SHELL
  #   yum update -y
  # SHELL
end
