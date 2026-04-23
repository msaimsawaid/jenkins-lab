def flag = true
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Project...'
            }
        }
        stage('Test') {
            when {
                expression { flag == true }
            }
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
            // This action will happen always regardless of the result of build
            echo 'Post build condition running'
        }
        failure {
            // This action will happen only if the build has failed
            echo 'Post Action if Build Failed'
        }
    }
} // This brace ends the entire pipeline [cite: 28, 29]
