pipeline {
    agent { dockerfile true } 
    stages{
	stage('Build') {
	    steps {
		sh '''
		docker run -p 8081:8081 IMAGEID
		'''
	    }
	}
    }
}
