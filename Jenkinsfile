pipeline {
    agent {
        docker {
            image 'nginx'
            args '-p 8080:80'
        }
    }
    environment {
        CI = 'true'
    }    
}
