Vagrant.configure('2') do |config|
  config.vm.define 'dev1' do |dev1|
    dev1.vm.box = 'ubuntu/trusty64'
    dev1.vm.hostname = 'dev1.local'
    dev1.vm.provision 'ansible' do |ansible|
      ansible.playbook = 'test.yml'
      ansible.sudo = true
      ansible.host_key_checking = false
    end  
  end
end
