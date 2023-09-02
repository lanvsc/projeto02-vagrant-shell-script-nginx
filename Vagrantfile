Vagrant.configure("2") do |config|
  #Configurando VM do Projeto 02
  config.vm.define:proj02 do |proj02_config|
    proj02_config.vm.box = "bento/ubuntu-22.04"
    proj02_config.vm.network "forwarded_port", guest: 80, host: 8080
    proj02_config.vm.network "public_network", ip: "192.168.100.155"
    proj02_config.vm.provision "shell", path: "script.sh"
    proj02_config.vm.synced_folder "site/" , "/var/www/html"
    proj02_config.vm.provider "virtualbox" do |v|
      v.gui = true
      v.memory = "1024"
      v.cpus = "1"
    end
  end
end