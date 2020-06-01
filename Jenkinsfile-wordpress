timestamps {

node () {

	stage ('simple-cicd - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/BINPIPE/simple-cicd-ec2.git']]]) 
	}
	stage ('simple-cicd - Build') {
 			// Shell build step
sh """ 
export ANSIBLE_HOST_KEY_CHECKING=False
cd ansible-playbooks/
ansible-playbook -i hosts -l Webserver, deploy-site.yml 
 """ 
	}
}
}
