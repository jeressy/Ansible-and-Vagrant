
  Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/trusty64"
    config.vm.box_version = "20191107.0.0"
  
  config.vm.synced_folder "./ansible", "/ansible"

  config.vm.provider "virtualbox" do |vb|
    vb.name= "fast-iac"
    vb.memory = "2048"
    vb.cpus = "2"
  end

  config.vm.network "forwarded_port", guest: 80, host: 8080, auto_correct:true

  config.vm.provision "shell" do |s|
    s.inline = <<-SHELL
      sudo apt-get update
      sudo apt-get install -y software-properties-common
      sudo apt-add-repository --yes --update ppa:ansible/ansible
      sudo apt-get install -y ansible
    SHELL
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "ansible/main.yml"
  end
end