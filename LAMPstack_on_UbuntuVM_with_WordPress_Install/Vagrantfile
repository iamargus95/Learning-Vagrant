# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  #box settings
  config.vm.box = "ubuntu/trusty64"

  #Provider Settings
  config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
     vb.memory = "2048"
     vb.cpus = 4
  end

  #Network Settings
  config.vm.network "forwarded_port", guest: 80, host: 1234
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"

  #Folder Settings
  # config.vm.synced_folder "../data", "/vagrant_data"

  #Provision Settings
  # config.vm.provision "shell", inline: <<-SHELL
  #    apt-get update
  #    apt-get install -y apache2
  #    apt install mysql-server
  #  SHELL
  config.vm.provision "shell", path: "bootstrap.sh"

end
