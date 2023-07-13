Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"
    config.vm.synced_folder "./ansible", "/ansible"
    config.vm.provision "shell", inline: <<-SHELL
      apt update
      apt install ansible -y
      ansible-playbook --connection=local /ansible/playbook.yml
      SHELL
end

