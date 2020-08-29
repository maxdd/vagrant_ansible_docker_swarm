# vagrant_ansible_docker_swarm
Let's use Vagrant to spawn 2 VMs with docker as a service in a manager/worker swarm combination
Docker-API shall be secure via tls client/server certificates

## How-to
To install Vagrand on Ubuntu
```
    sudo apt update 
    sudo apt install virtualbox
    curl -O https://releases.hashicorp.com/vagrant/2.2.10/vagrant_2.2.10_x86_64.deb
    sudo apt install ./vagrant_2.2.10_x86_64.deb
    vagrant --version
```

To start Vagrand project (in the root of Vagrantfile)
```
vagrant up
```

## TODO
- Secure docker-api with tls certificates
- Swarm setup