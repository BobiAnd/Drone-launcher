pipeline {
    agent any
    stages {
	stage('Launch launcher') {
	    steps {
		bat 'python dronelauncher_python.py &&'
		bat 'timeout 5 >nul ; safeExit'
            }
	}
    }
}
