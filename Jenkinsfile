timestamps {

node () {

	stage ('SBA_python_flask - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/DanyYanez/sba.jenkins-github-pipeline']]])
	}
	stage ('SBA_python_flask - Build') {

sh """
apt install python3
python3 web.py
 """
	}
}
}
