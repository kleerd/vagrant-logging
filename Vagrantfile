VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'ubuntu-server-12.04'
  config.vm.network :private_network, ip: '192.168.111.222'
  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'playbook.yml'
    ansible.inventory_path = 'hosts'
    ansible.limit = 'all'
  end
end

