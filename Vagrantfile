Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "public_network", ip: "192.168.1.35"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "8096"
    vb.cpus = 2
  end

  config.vm.provision "shell", inline: <<-SHELL
    # Ajout du repository Docker
    sudo yum install -y yum-utils device-mapper-persistent-data lvm2
    sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

    # Installation de Docker
    sudo yum install -y docker-ce docker-ce-cli containerd.io

    # Activation de Docker au démarrage
    sudo systemctl enable docker

    # Démarrage du service Docker
    sudo systemctl start docker
  SHELL
end
