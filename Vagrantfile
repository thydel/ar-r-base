# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  config.vm.define 'r-base' do |c|
    c.vm.box = 'debian-wheezy'
    c.vm.network :private_network, ip: '192.168.99.2'
    c.vm.hostname = 'r-base.local'
    c.vm.provision 'ansible' do |ansible|
      ansible.playbook = 'test.yml'
      ansible.sudo = true
      ansible.inventory_path = 'vagrant-inventory'
      # https://github.com/mitchellh/vagrant/issues/5017
      ansible.raw_ssh_args = ['-o IdentitiesOnly=yes']
      # http://docs.vagrantup.com/v2/provisioning/ansible.html
      # ansible.host_key_checking = false
    end
  end
end
