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
                          cscript /nologo sleep.js 5000; exit

                    }
                }

                    }
    }
}
}