pipeline {
    agent any
    stages {
	stage('Launch launcher') {

                   parallel{
                       stage ('Deploy to Staging'){
                           steps
                            sh  bat 'python dronelauncher_python.py'

             }
            }
             stage ("exiting program"){
                 steps {
                                     bat 'sleep 60 ; exit'


                }

                    }
    }
}
}