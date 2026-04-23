pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Project...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing Project...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Project...'
            }
        }
    } // This brace ends the stages section [cite: 29]

    post {
        always {
            echo 'Post build condition running' [cite: 53, 54, 55]
        }
        failure {
            echo 'Post Action if Build Failed' [cite: 54]
        }
    }
} // This brace ends the entire pipeline [cite: 28, 29]
