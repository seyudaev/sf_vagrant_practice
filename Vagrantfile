
Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-18.04"

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
	sudo apt install -y software-properties-common
	sudo apt update
	sudo apt install -y python3.8
	sudo apt install -y python3-pip
	sudo apt update
	sudo apt install -y libpq-dev python-dev
	sudo pip3 install psycopg2
	sudo apt install python3-django
	python3 --version
  SHELL
  config.vm.provision "file", source: "~/Documents/Skillfactory-Devops/vagrant/ProjectWork10/testfile", destination: "$HOME/remote/test"
end