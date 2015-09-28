# -*- mode: ruby -*-
# vi: set ft=ruby :

Dotenv.load

# change default provider to digital_ocean
ENV['VAGRANT_DEFAULT_PROVIDER'] = "digital_ocean"

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.provider :digital_ocean do |provider, override|


    override.ssh.private_key_path = '~/.ssh/vagrant_rsa.pem'
    override.vm.box = 'digital_ocean'
    override.vm.box_url = "https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box"

    provider.token = '0bb42d2ed30031593dcf3b457cadf1624641e951ab4ab2cb2a80cac007693677'
    provider.image = 'ubuntu-14-04-x64'
    provider.region = 'sgp1'
    provider.size = '512mb'

    #
    # override.vm.hostname          = "vagrant-do-test"
    # override.vm.box               = "digital_ocean"
    # override.vm.box_url           = "https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box"
    # override.ssh.private_key_path = "#{ENV['DO_SSH_KEY']}"
    # override.ssh.username         ="#{ENV['DO_SSH_USERNAME']}"
    #
    # provider.ssh_key_name         = 'Vagrant'
    # provider.client_id            = "#{ENV['DO_CLIENT_ID']}"
    # provider.api_key              = "#{ENV['DO_API_KEY']}"
    # provider.token                = "#{ENV['DO_API_TOKEN']}"
    #
    # provider.region               = "Singapore 1"
    # provider.image                = "CentOS 6.5 x64"
    # provider.size                 = "512MB" # 512MB | 1GB | 2GB | 4GB | 8GB | 16GB
    # # provider.image = "CentOS 7.0 x64"
    # # provider.region = "sgp1"
    # # provider.size = "512MB"
    #
    # provider.private_networking   = true
    # provider.setup                = true

    # provider.ca_path              = '/usr/local/opt/curl-ca-bundle/share/ca-bundle.crt'
    # provider.ca_path              = "/usr/local/share/ca-bundle.crt"
    # disable synced_folder: rsync is not installed on DigitalOcean's guest machine
    # override.vm.synced_folder "./", "/vagrant", disabled: true

    # if ENV['WERCKER'] == "true"
    # 	provider.ssh.key_name = "wercker"
    # else
    # 	provider.ssh.key_name = "winpc"
    # end
  end
end
