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

	stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
}
