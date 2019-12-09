pipeline {
    agent {
        docker {
            image 'nginx'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
    }    
    stages{
	stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
