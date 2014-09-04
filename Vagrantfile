# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 80, host: 8469

  config.vm.provision "docker" do |d|
    d.pull_images "ubuntu"
  end
  # config.vm.synced_folder "sites-available", "/etc/nginx/sites-available"
  # config.vm.provision :shell, :path => "bootstrap.sh"
end
