# -*- mode: ruby -*-

Vagrant.configure("2") do |config|
  ## Use the Vagrant box for the latest Ubuntu LTS version.
  config.vm.box = "ubuntu/focal64"

  ## Disable the default folder sharing/syncing.
  config.vm.synced_folder ".", "/vagrant", disabled: true

  ## Configure provider.
  config.vm.provider "virtualbox" do |v|
    ## Set MEM of 4GB.
    v.memory = 1024

    ## Set 2 CPUs.
    v.cpus = 1
  end
end
