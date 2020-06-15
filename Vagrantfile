# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    # /*=====================================
    # =            FREE VERSION!            =
    # =====================================*/
    # This is the free (still awesome) version of Scotch Box.
    # Please go Pro to support the project and get more features.
    # Check out https://box.scotch.io to learn more. Thanks

    # automatic guest plugin update disabled
    if Vagrant.has_plugin?("vagrant-vbguest")
        config.vbguest.auto_update = false
    end

    config.vm.box = "scotch/box"
    config.vm.box_check_update = false
    config.vm.network "private_network", ip: "192.168.33.10"
    config.vm.hostname = "scotchbox"
    config.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]

    # Optional NFS. Make sure to remove other synced_folder line too
    #config.vm.synced_folder ".", "/var/www", :nfs => { :mount_options => ["dmode=777","fmode=666"] }

    # VirtualBox specific settings
    config.vm.provider "virtualbox" do |virtualbox|
        # friendly name of the virtual machine
        virtualbox.name = "Scotch.Box"
        # Hide/show the VirtualBox GUI when booting the machine
        virtualbox.gui = true
        # Customize the amount of memory 4GB on the VM:
        virtualbox.memory = 4096
        # Use 2 CPUs in the VM:
        virtualbox.cpus = 2
    end

end
