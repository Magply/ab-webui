VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "bento/ubuntu-18.04"
  config.vm.hostname = "ab-webui"
  config.vm.network "private_network", ip: "172.10.10.12"
  # Set the memory size
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 2048
  end

  # Install the Ansible provisioner
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yaml"
    ansible.verbose = true
  end
end
