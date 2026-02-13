Vagrant.configure("2") do |config|
  config.vm.define "control" do |control|
    control.vm.box = "ubuntu/bionic64"
    control.vm.hostname = "control"
    control.vm.network "private_network", ip: "192.168.56.10"
    control.vm.provision "shell", inline: <<-SHELL
      apt update
      apt install -y ansible sshpass
    SHELL
  end

  config.vm.define "web1" do |web1|
    web1.vm.box = "ubuntu/bionic64"
    web1.vm.hostname = "web1"
    web1.vm.network "private_network", ip: "192.168.56.11"
    web1.vm.provision "shell", inline: <<-SHELL
      apt update
      apt install -y python3 apache2
    SHELL
  end

  config.vm.define "web2" do |web2|
    web2.vm.box = "ubuntu/bionic64"
    web2.vm.hostname = "web2"
    web2.vm.network "private_network", ip: "192.168.56.12"
    web2.vm.provision "shell", inline: <<-SHELL
      apt update
      apt install -y python3 apache2
    SHELL
  end
end
