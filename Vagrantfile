Vagrant.configure("2") do |config|
  config.vm.box = "psysdev/basebox-ubuntu-16.04-java8-mysql"
  config.vm.box_check_update = false
  config.vm.box_version = "1.0"
  config.vm.network :forwarded_port, guest: 3306, host: 3306
  config.vm.provision :shell, :path => "install.sh"
  config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777", "fmode=666"]
  config.vm.network "private_network", ip: "10.19.17.12" 
end