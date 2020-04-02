

pipeline {
    agent any
    stages {
	stage('Launch launcher')
	('Checkout') {
	    steps {
		bat 'python dronelauncher_python.py'
		 git 'https://github.com/BobiAnd/Drone-launcher'
		  }
                           }

             stage('Build') {
               steps {
                 sh "mvn -B compile"
                  }
                    }
                stage('Test') {
                 steps {
                   sh "mvn -B test"
                    chuckNorris()
            }
	}
    }
    
    post {
        always {
            junit '**/TEST*.xml'
            emailext attachLog: true, attachmentsPattern: '**/TEST*xml',
	    body: 'Bod-DAy!', recipientProviders: [culprits()], subject:
            '$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS!'
	}
    }
}
