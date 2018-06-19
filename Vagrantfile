Vagrant.configure("2") do |config|

  config.vm.box = "bento/ubuntu-16.04"
  config.vm.provider :virtualbox do |vb, override|
    override.vm.box = "bento/ubuntu-16.04"
  end

  config.vm.box_check_update = false


  config.vm.define :repo, autostart: false do |use_ansible|
    ## Run Ansible from the Vagrant Host:
    use_ansible.vm.provision "ansible" do |ansible|
      ansible.playbook = "bug.yaml"
    end
  end
end
