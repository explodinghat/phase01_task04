Vagrant.configure("2") do |config|
  #Base OS Configuration
  config.vm.box = "generic/ubuntu2004"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant"
  config.ssh.username = "vagrant"

  #Ansible Slave 0
  config.vm.define "ansible-slave0" do |ansibleslave0|
    ansibleslave0.vm.network "private_network", ip: "192.168.50.2"
    ansibleslave0.vm.hostname = "ansible-slave0"

    #General VM Config
    ansibleslave0.vm.provider "virtualbox" do |v|
      v.gui = false
      v.memory = 1024
      v.linked_clone = false
      v.name = "ansible-slave0"
    end
  end

  #Ansible Slave 1
  config.vm.define "ansible-slave1" do |ansibleslave1|
    ansibleslave1.vm.network "private_network", ip: "192.168.50.3"
    ansibleslave1.vm.hostname = "ansible-slave1"

      #General VM Config
      ansibleslave1.vm.provider "virtualbox" do |v|
        v.gui = false
        v.memory = 1024
        v.linked_clone = false
        v.name = "ansible-slave1"
    end
  end

end
