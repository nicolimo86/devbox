Vagrant.configure("2") do |config|
  config.vm.define :vm1 do |vm1|
      vm1.vm.box = "ubuntu/bionic64"
      vm1.vm.provider "virtualbox" do |box|
          box.memory = 4086 
      end
      vm1.vm.provision :hosts, :sync_hosts => true
      vm1.vm.synced_folder "~/workspace", "/workspace"
      vm1.vm.synced_folder "~/.aws", "/aws"
      vm1.disksize.size = '15G'
  end
  #config.vm.network "forwarded_port", guest: 8081, host: 8081
  config.vm.provision "ansible_local" do |ansible|
    ansible.verbose = "v"
    ansible.install_mode = "pip3"
    #ansible.version = "2.9.19"
    ansible.galaxy_role_file = "./ansible/requirements.yml"
    ansible.galaxy_roles_path = "./ansible/.external_roles:./ansible/roles"
    ansible.playbook = "ansible/playbook.yml"
  end
end
