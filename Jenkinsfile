pipeline {
    agent any
    stages {
	stage('Launch launcher') {
	    steps {
	     parallel(
             "Status Code": {
            bat 'python dronelauncher_python.py'

             },
              "exiting program": {
             bat 'sleep 60 ; exit')



            }

    }
}
}