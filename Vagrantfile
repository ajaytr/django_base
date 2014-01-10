# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config| 
    # All Vagrant configuration is done here. The most common configuration
    # options are documented and commented below. For a complete reference,
    # please see the online documentation at vagrantup.com.

    config.vm.define :djangovm do |django_config|
        # Every Vagrant virtual environment requires a box to build off of.
        django_config.vm.box = "precise64"

        # The url from where the 'config.vm.box' box will be fetched if it
        # doesn't already exist on the user's system.
        config.vm.box_url = "http://files.vagrantup.com/precise64.box"
        
        # Create a forwarded port mapping which allows access to a specific port
        # within the machine from a port on the host machine. In the example below,
        # accessing "localhost:8080" will access port 80 on the guest machine.
        django_config.vm.network :forwarded_port, host: 8080, guest: 80
        django_config.vm.network :forwarded_port, host: 8001, guest: 8000

        # Enable provisioning with chef solo, specifying a cookbooks path, roles
        # path, and data_bags path (all relative to this Vagrantfile), and adding
        # some recipes and/or roles.
        #
        django_config.vm.provision :chef_solo do |chef|
            chef.cookbooks_path = "cookbooks"
            chef.add_recipe "apt"
            chef.add_recipe "apache2::mod_wsgi"
            chef.add_recipe "build-essential"
            chef.add_recipe "git"
            chef.add_recipe "vim"
        
            # You may also specify custom JSON attributes:
            # chef.json = { :mysql_password => "foo" }
        end
    end
end
