timestamps {

node () {

	stage ('SBA_python_flask - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/DanyYanez/sba.jenkins-github-pipeline']]])
	}
	stage ('SBA_python_flask - Build') {

sh """
cd ~
kind create cluster --name pipeline-project --config kubernetes.yaml
kind load docker-image danyyanez/sba_kuber
#python3 web.py
 """
	}
}
}
