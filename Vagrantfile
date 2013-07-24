Vagrant.require_plugin "vagrant-chef-zero"
Vagrant.require_plugin "vagrant-berkshelf"

Vagrant.configure("2") do |config|
  config.berkshelf.enabled = true
  config.chef_zero.chef_repo_path = "spec/vagrant-chef-zero/fixtures/"
  #config.chef_zero.nodes =        "spec/vagrant-chef-zero/fixtures/nodes"
  #config.chef_zero.environments = "spec/vagrant-chef-zero/fixtures/environments"
  #config.chef_zero.data_bags =    "spec/vagrant-chef-zero/fixtures/data_bags"
  #config.chef_zero.cookbooks =    "spec/vagrant-chef-zero/fixtures/cookbooks"
  #config.chef_zero.roles = "foobar"

  config.vm.box = "Berkshelf-CentOS-6.3-x86_64-minimal"
  config.vm.box_url = "https://dl.dropbox.com/u/31081437/Berkshelf-CentOS-6.3-x86_64-minimal.box"
  #config.vm.box = ENV['YIPIT_VAGRANT_BOX']
  config.vm.provision :chef_client do |chef|
    chef.run_list = [
    ]
  end
end
