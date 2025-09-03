# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"

  # Common settings for all VMs
  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 1
    vb.memory = 1024
  end

  # Machine 1: jarawinshin
  config.vm.define "jarawinshin" do |jarawinshin|
    jarawinshin.vm.hostname = "jarawinshin"
    jarawinshin.vm.network "private_network", ip: "192.168.56.250"

  end
end
