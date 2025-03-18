pipeline {
    agent any

    stages {
        // Build Stage
        stage('Build') {
            steps {
                script {
                    sh 'g++ hello.cpp -o PES1UG22CS528-1'
                }
            }
        }

        // Test Stage
        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS528-1'
                }
            }
        }

        // Deploy Stage
        stage('Deploy') {
            steps {
                echo 'Deployment successful!'
            }
        }
    }

    // Post Conditions
    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}
