pipeline {
  agent any
  stages {
    stage('Build') {
	    steps {
		    sh 'printenv'
		    sh 'ant -f build.xml -v'
		    }
			}
    stage('Post-Build') {
	    steps { 
		    archiveArtifacts artifacts: 'dist/*.war',fingerprint :true
	    }
		}
    }
	}
