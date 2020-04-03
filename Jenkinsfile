pipeline {
    agent any
    stages {
	stage('Launch launcher') {
	    steps {
		sh 'python dronelauncher_python.py &'
		sh 'sleep 60 ; exit'
            }
	}
    }
}
