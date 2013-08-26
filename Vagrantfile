# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config| 

  config.vm.box = "centos64"
  config.vm.hostname = "ezp5.vagrant"
  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  # config.vm.box_url = "http://domain.com/path/to/above.box"
  config.vm.box_url = "http://puppet-vagrant-boxes.puppetlabs.com/centos-64-x64-vbox4210.box"
 
  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # Unable to use due to issue https://github.com/mitchellh/vagrant/issues/1777
  # config.vm.network :private_network, ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # Without the use of this, eZ Publish won't be able to get the site packages using Windows and Mac OS Hosts
  config.vm.network :public_network

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  config.vm.provider :virtualbox do |vb|
  # Don't boot with headless mode
  #   vb.gui = true
  #
  #   # Use VBoxManage to customize the VM. For example to change memory:
  #  vb.customize ["modifyvm", :id, "--memory", "1024"]
  vb.customize ["modifyvm", :id, "--memory", "512"]
  end
end