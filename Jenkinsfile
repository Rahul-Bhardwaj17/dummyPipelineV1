pipeline {
    agent any

    tools {
        maven 'myMaven'
        jdk 'myJAVAJDK'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the application...'
                    // Assuming your App.java is in the specified location
                    sh 'clean install'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    echo 'Running tests...'
                    sh 'mvn test'
                }
            }
        }

        stage('Deploy') {
    steps {
        script {
            echo 'Deploying the application to Tomcat...'
            // Replace the following with your deployment steps

            // Example: Deploying to Tomcat using the manager-script role
            sh 'curl -v -u tomcat:tomcat -T target/dummyPipelineProjectV1.war http://localhost:8081/manager/text/deploy?path=/dummyPipelineProjectV1&update=true'

            // Replace 'dummyPipelineProjectV1' with the context path of your application

            // Add your actual deployment commands here
        }
    }
}
    }

    post {
      
        success {
            echo 'Tests passed! Send notifications or perform additional actions here.'
        }
        failure {
            echo 'Tests failed! Send notifications or perform cleanup actions here.'
        }
    }
}
