pipeline {
    agent { dockerfile true } 
    stages{
	stage('Build') {
	    steps {
		sh 'docker build -t app:test .'
	    }
	}
	stage('Test') {
	    steps {
		echo 'Test'
		sh 'docker run -p 80:80 --name app INTEGRACIONCONTINUA/app:test'
		sh 'nc -vz localhost 80'
		sh 'docker stop app'
	    }
	}
    }
}
