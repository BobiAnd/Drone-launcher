pipeline {
    agent any
    stages {
    stage('build') {
     steps {
      dir("build_folder"){
          bat "run_build_windows.bat"
      }
    }
    }
	stage('Launch launcher') {
	    steps {
		bat 'python dronelauncher_python.py &'
		bat 'TIMEOUT /T 30'
            }
	}
    }
}
