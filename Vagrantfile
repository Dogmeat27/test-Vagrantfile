# Create new vagrant box
Vagrant.configure("2") do |config|
  # Base VM config
  config.vm.box = "generic/ubuntu2004"
  config.vm.hostname = "ubuntu2004"

  # Configuring exposed ports
  config.vm.network "forwarded_port", guest: 3000, host: 3000, host_ip: "127.0.0.1"

  # Run ansible test playbook
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "test.yml"
  end
end
