pipeline {
    agent any
    stages {
	stage('Launch launcher') {
	    steps {
		bat 'python dronelauncher_python.py &&'
		bat 'timeout(time: 30, unit: 'SECONDS') ; EXIT'
            }
	}
    }
}
