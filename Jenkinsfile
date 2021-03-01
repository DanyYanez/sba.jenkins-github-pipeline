timestamps {

node () {

	stage ('SBA_python_flask - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/DanyYanez/sba.jenkins-github-pipeline']]])
	}
	stage ('SBA_python_flask - Build') {

sh """
kubectl exec --stdin --tty flaskapp-5ff668455-kr584 -- /bin/bash
python3 web.py
 """
	}
}
}
