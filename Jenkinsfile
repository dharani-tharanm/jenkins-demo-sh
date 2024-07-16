pipeline {
    agent any // This runs the pipeline on any available agent/node

    stages {
        stage('Restore') {
            steps {
                echo 'Building (restore) the project...'
                sh 'dotnet restore'
            }
        }
        stage('Build') {
            steps {
                echo 'Building tests...'
                sh 'dotnet build' // Example Maven test step
            }
        }
    }

    post {
        success {
            echo 'Pipeline  for CI succeeded! Yay!'
            // Additional actions on success, if any
        }
        failure {
            echo 'Pipeline for CI failed! :('
            // Additional actions on failure, if any
        }
    }
}
