pipeline {
    agent { dockerfile true } 
    stages{
	stage('Build') {
	    steps {
		sh 'docker build -t app:test IntegracionContinua .'
	    }
	}
	stage('Test') {
	    steps {
		echo 'Test'
		sh 'docker run -d -p 80:80 --rm --name app app:test'
		sh 'nc -vz localhost 80'
		sh 'docker stop app'
	    }
	}
    }
}
