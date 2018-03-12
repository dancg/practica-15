# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
 # Load Balancer
  config.vm.define "web-balancer" do |app|
    app.vm.hostname = "Nginx"
    #app.vm.network "public_network"
    app.vm.network "private_network", ip: "192.168.33.10"
    app.vm.provision "shell", path: "provision/nginx.sh"
  end

  # Nginx Server
  config.vm.define "web-1" do |app|
    app.vm.hostname = "web-1"
    #app.vm.network "public_network"
    app.vm.network "private_network", ip: "192.168.33.11"
    app.vm.provision "shell", path: "provision/nginx1.sh"
  end

  # Nginx Server
  config.vm.define "web-2" do |app|
    app.vm.hostname = "web-2"
    #app.vm.network "public_network"
    app.vm.network "private_network", ip: "192.168.33.12"
    app.vm.provision "shell", path: "provision/nginx1.sh"
  end

end