Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-5.11-i386"
  config.vm.network "private_network", type: "dhcp"
  config.omnibus.chef_version = :latest
  config.vm.provision :chef_client do |chef|
    chef.provisioning_path = "/etc/chef"
    chef.chef_server_url = "https://api.chef.io/organizations/inno-unigo"
    chef.validation_key_path = ".chef/saichinn25.pem"
    chef.validation_client_name = "saichinn25"
    chef.node_name = "centos-server"
    chef.add_recipe "webserver"
  end
end
