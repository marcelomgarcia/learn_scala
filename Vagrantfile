# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "debian/bookworm64"
  config.vm.hostname = "scalabox"
  config.vm.provider "virtualbox" do |vb|
    # Customize the amount of memory on the VM:
    vb.memory = "4096"
    vb.cpus = 4

  end
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y git curl unzip vim python-is-python3 python3-venv zip
    echo "alias ll='ls -lh'" > /home/vagrant/.bash_aliases
    chown vagrant:vagrant /home/vagrant/.bash_aliases
  SHELL
end