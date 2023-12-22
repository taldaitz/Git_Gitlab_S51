Vagrant.configure("2") do |config|

    config.vm.define "gitlab" do |gitlab|
        gitlab.vm.box = "generic/ubuntu2204"
        gitlab.vm.network "forwarded_port", guest: 80, host: 8080
        gitlab.vm.network :private_network, ip: "10.0.0.10"
        gitlab.vm.hostname = "gitlab"
    end

    config.vm.define "prod" do |prod|
        prod.vm.box = "generic/ubuntu2204"
        prod.vm.network "forwarded_port", guest: 80, host: 9090
        prod.vm.network :private_network, ip: "10.0.0.11"
        prod.vm.hostname = "prod"
    end
end