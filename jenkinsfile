pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Add your build steps here
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add your deployment steps here
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! Send notifications or perform additional actions here.'
        }
        failure {
            echo 'Pipeline failed! Send notifications or perform cleanup actions here.'
        }
    }
}
