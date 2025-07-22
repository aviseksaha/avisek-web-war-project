pipeline {
	agent any
	stages{
		stage('stage-1') {
			steps {
				echo "Hello World !"
			}
		}
	}
}

pipeline {
    agent any
	
	environment{
		PATH = "/opt/maven/bin:$PATH"
	}
	
	
    stages {
		stage('git clone') {
			steps {
				git url: 'https://github.com/aviseksaha/avisek-web-war-project.git', 'branch': 'main'
			}
		}
		
		stage('build') {
            steps {
                sh 'mvn deploy'
            }
        }
	}
}
