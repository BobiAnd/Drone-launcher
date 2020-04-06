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
                       bat  "ping 127.0.0.1 -n1 -w 30000 >NUL"
                        exit
                       }

                    }
                }

                    }
    }
}
