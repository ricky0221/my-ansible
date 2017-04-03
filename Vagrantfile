Vagrant.configure("2") do |config|
	# Server: jenkins_server
	config.vm.define :jenkins_server do |jenkins_config|
		jenkins_config.vm.box = "bento/ubuntu-15.10"
		jenkins_config.vm.network "forwarded_port", guest: 8080, host: 9080

		# run Ansible playbook from Vagrant host
		jenkins_config.vm.provision "ansible" do |ansible|
			ansible.playbook = "playbook.yml"
		end
	  end

	# Server: jenkins_target
	# config.vm.define :jenkins_target do |jenkins_target_config|
	# 	jenkins_target_config.vm.box = "bento/ubuntu-15.10"
	#   end
end
