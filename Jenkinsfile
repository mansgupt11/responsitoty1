pipeline {
    agent any
    stages {
        stage('hello') {
            steps {
                echo 'Test hello world 2'
            }
        }
        stage('GitcheckPipeline') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/mansgupt11/responsitoty1.git']]])
            }
		}
		 stage('runShellScript') {
            steps {
          sh '''cd /root
          ./deploy.sh'''      
            }
		}
		}
}
