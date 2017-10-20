# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-7.4"

  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true
  config.ssh.insert_key = false

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
  end

  config.vm.provision "shell", inline: "systemctl restart network.service"

  config.vm.define "vuls01" do |vuls|
    vuls.vm.hostname = "vuls.vagrant.com"
    vuls.vm.network "private_network", ip: "192.168.33.33"

    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "site.yml"
      ansible.inventory_path = "inventory/hosts"
      ansible.limit = 'vagrant'
      ansible.verbose = "v"
    end
  end

end
