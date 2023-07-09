Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "public_network", ip: "192.168.1.35"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "8096"
    vb.cpus = 2
  end

  config.vm.provision "shell", inline: <<-SHELL
    
  SHELL
end
