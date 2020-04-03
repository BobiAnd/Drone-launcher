pipeline {
    agent any
    stages {
	stage('Launch launcher') {
	    steps {
		bat 'python dronelauncher_python.py &'
		bat 'TIMEOUT /T 30'
            }
	}
    }
}
