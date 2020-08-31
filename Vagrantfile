Vagrant.configure(2) do |config|
    config.vm.box = "centos/7"
    config.disksize.size = '40GB' # requires vagrant-disksize plugin

    config.vm.define "docker_swarm_1" do |docker_swarm_1|
      # Let's move ssh guest port to a known one
      #docker_swarm_1.vm.network "forwarded_port", guest: 22, host: 1336, id: 'ssh' #ssh vagrant@127.0.0.1 -p 1336 -i .vagrant/machines/docker_swarm_1/virtualbox/private_key
      docker_swarm_1.vm.hostname = "docker-swarm-1"
      docker_swarm_1.vm.network "private_network", ip: '192.168.55.10'
    end
  
    config.vm.define "docker_swarm_2" do |docker_swarm_2|
      # Let's move ssh guest port to a known one
      #docker_swarm_2.vm.network "forwarded_port", guest: 22, host: 1337, id: 'ssh'
      docker_swarm_2.vm.hostname = "docker-swarm-2"
      docker_swarm_2.vm.network "private_network", ip: '192.168.55.20' #ssh vagrant@192.168.55.20 -p 22 -i .vagrant/machines/docker_swarm_2/virtualbox/private_key 
    end

  end