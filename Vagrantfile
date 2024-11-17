# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Imagen base de Debian Bookworm
  config.vm.box = "debian/bookworm64"

  # Configuración común: actualizar e instalar paquetes de DNS
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y bind9 dnsutils
  SHELL

  # Máquina DNSA (Maestro)
  config.vm.define "dnsa" do |dnsa|
    # Nombre de host
    dnsa.vm.hostname = "dnsa"
    
    # Red privada con IP estática
    dnsa.vm.network "private_network", ip: "192.168.57.10"

    # Configurar para que si después de cierto tiempo no se inicializa, detenerlo
    dnsa.vm.boot_timeout = 180

    # Configuración específica del proveedor VirtualBox
    dnsa.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
    end

    # Copiar archivos de configuración de zona
      dnsa.vm.provision "shell", inline: <<-SHELL
      sudo cp -v /vagrant/files/MASTER.ies.test.dns /etc/bind/MASTER.ies.test.dns
      sudo cp -v /vagrant/files/MASTERnamed.conf.local /etc/bind/named.conf.local
      sudo systemctl restart bind9
    SHELL
  end

  # Máquina DNSB (Esclavo)
  config.vm.define "dnsb" do |dnsb|
    # Nombre de host
    dnsb.vm.hostname = "dnsb"
    
    # Red privada con IP estática
    dnsb.vm.network "private_network", ip: "192.168.57.11"

    # Configurar para que si después de cierto tiempo no se inicializa, detenerlo
    dnsb.vm.boot_timeout = 180

    # Configuración específica del proveedor VirtualBox
    dnsb.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
    end

    # Copiar archivos de configuración de zona
    dnsb.vm.provision "shell", inline: <<-SHELL
    sudo cp -v /vagrant/files/SLAVEnamed.conf.local /etc/bind/named.conf.local
    sudo systemctl restart bind9
  SHELL
  end
end