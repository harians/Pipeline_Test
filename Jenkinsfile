pipeline {
  agent any
  stages {
    stage('Build_Stage') {
	    steps {
		    sh 'printenv'
		    sh 'ant -f build.xml -v'
		    }
			}
    stage('Post-Build_Stage') {
	    steps { 
		    archiveArtifacts artifacts: 'dist/*.war',fingerprint :true
	    }
		}
    }
	}
