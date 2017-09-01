# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  config.vm.hostname = 'users'
  config.vm.box = 'kapke/xenial64-lxc'

  config.ssh.forward_agent = true

  config.vm.provider :lxc do |lxc|
    lxc.container_name = 'users'
  end

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'test/test.yml'
    # ansible.galaxy_role_file  = 'provision/galaxy.yml'
  end
end
