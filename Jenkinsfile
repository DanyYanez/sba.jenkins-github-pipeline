timestamps {

node () {

	stage ('SBA_python_flask - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/DanyYanez/sba.jenkins-github-pipeline']]])
	}
	stage ('SBA_python_flask - Build') {

sh """

kind create cluster --name final-project --config kind-config.yaml
kind load docker-image danyyanez/sba_kuber
#python3 web.py
 """
	}
}
}
