pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ working.cpp -o output' // Compile the C++ file into an executable named 'output'
                echo 'Build stage completed'
            }
        }
        stage('Test') {
            steps {
                sh './output' // Run the compiled executable to test it
                echo 'Test stage completed'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...' // Simulate deployment with a message
                echo 'Deploy stage completed'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed' // Display this message if any stage fails
        }
        success {
            echo 'Pipeline completed successfully' // Optional: Added for confirmation
        }
    }
}
