# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.hostname = "users"
  config.vm.box = "plumelo/xenial64"

  config.vm.provider :lxc do |lxc, override|
    lxc.container_name = "users"
  end

  # config.vm.provision 'ansible' do |ansible|
  #   ansible.playbook = 'test.yml'
  # end
  config.vm.provision "shell",
    :path => "specs.sh",
    :upload_path => "/home/vagrant/specs",
    # change role name below
    :args => "--install ansible-role-users"
end
