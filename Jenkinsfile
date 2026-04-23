def flag = true 

pipeline {
    agent any

    // Step 9: Define environment variables
    environment {
        NEW_VERSION = '1.3.0'
    }

    // Step 10: Define build parameters
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Check to run the Test stage')
    }

    stages {
        stage('Build') {
            steps {
                // Using the environment variable from Step 9
                echo "Building version ${env.NEW_VERSION}"
            }
        }
        stage('Test') {
            // Step 8 & 10: Conditional execution using 'when'
            when {
                expression { flag == true && params.executeTests == true }
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
    }

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
