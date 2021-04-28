Vagrant.configure("2") do |config|
  config.vm.define :devbox do |devbox_config|
      devbox_config.vm.box = "ubuntu/bionic64"
      devbox_config.vm.provider "virtualbox" do |box|
          box.memory = 4086 
      end
      devbox_config.vm.provision :hosts, :sync_hosts => true
      devbox_config.vm.synced_folder "~/workspace", "/home/vagrant/workspace"
      devbox_config.vm.synced_folder "~/.aws", "/home/vagrant/.aws"
      devbox_config.disksize.size = '15G'
  end
  #config.vm.network "forwarded_port", guest: 8081, host: 8081
  config.vm.provision "ansible_local" do |ansible|
    ansible.verbose = "v"
    #ansible.install_mode = "pip" #it fails on bionic (python 3.6+ required). Ansible will be installed via apt.
    #ansible.version = "2.9.19" #to be use if install_mode works
    ansible.galaxy_role_file = "./ansible/requirements.yml"
    ansible.galaxy_roles_path = "./ansible/.external_roles:./ansible/roles"
    ansible.playbook = "ansible/playbook.yml"
  end
end
