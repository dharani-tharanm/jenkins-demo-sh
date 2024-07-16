pipeline {
    agent any // This runs the pipeline on any available agent/node

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'mvn clean package' // Example Maven build step
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test' // Example Maven test step
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! Yay!'
            // Additional actions on success, if any
        }
        failure {
            echo 'Pipeline failed! :('
            // Additional actions on failure, if any
        }
    }
}
