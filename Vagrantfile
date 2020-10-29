Vagrant.configure("2") do |config|
	config.vm.define "alura-web" do |web|
		web.vm.box = "ubuntu/bionic64"
		web.vm.provision "shell", path: "assets/install.sh"
		web.vm.provision "file", source: "assets/apache-tomcat-8.5.47.tar.gz", destination: "/tmp/apache-tomcat-8.5.47.tar.gz"
		web.vm.provision "file", source: "assets/tomcat.service", destination: "/tmp/tomcat.service"
		web.vm.provision "shell", path: "assets/post-install.sh"
	end
end