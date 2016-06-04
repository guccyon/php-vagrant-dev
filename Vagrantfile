Vagrant.configure(2) do |config|
  config.ssh.insert_key = false
  config.vm.box = "centos/7"

  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.synced_folder ".", "/var/www/myapp",
    mount_options: ["dmode=775,fmode=666"]

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
  end
end
