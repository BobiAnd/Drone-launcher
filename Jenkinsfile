pipeline {
    agent any
    stages {
	stage('Launch launcher') {

                   parallel{
                       stage ('Deploy to Staging'){
                           steps{
                                bat 'python dronelauncher_python.py'

             }
            }
             stage ("exiting program"){
                 steps {
                       bat  'TIMEOUT /T 30 : exit'
                       }

                    }
                }

                    }
    }
}
