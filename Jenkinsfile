timestamps {

node () {

	stage ('simple-cicd - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/BINPIPE/simple-website.git']]]) 
	}
	stage ('simple-cicd - Build') {
 			// Shell build step
sh """ 
rm -rf simple-cicd-ec2
git clone https://github.com/BINPIPE/simple-cicd-ec2.git
cd simple-cicd-ec2/ansible-playbooks/
ansible-playbook -i hosts -l Webserver, deploy-site.yml 
 """ 
	}
}
}
