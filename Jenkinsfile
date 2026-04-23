def flag = true // From Step 8

pipeline {
    agent any

    // Step 9: Define custom environment variables [cite: 68]
    environment {
        NEW_VERSION = '1.3.0' 
    }

    // Step 10: Define build parameters [cite: 93]
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Check to run the Test stage')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building Project...'
                // Using the environment variable [cite: 71]
                echo "Building version ${env.NEW_VERSION}" 
            }
        }
        stage('Test') {
            // Combined Conditionals (Step 8 & 10) [cite: 58, 94]
            when {
                expression { flag == true && params.executeTests == true }
            }
            steps {
                echo 'Testing Project...'
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
