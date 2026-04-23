pipeline {
    agent any [cite: 29]
    stages { [cite: 29]
        stage('Build') { [cite: 29]
            steps {
                echo 'Building Project...' [cite: 29]
            }
        }
        stage('Test') { [cite: 29]
            steps {
                echo 'Testing Project...' [cite: 29]
            }
        }
        stage('Deploy') { [cite: 29]
            steps {
                echo 'Deploying Project...' [cite: 29]
            }
        }
    } // End of stages [cite: 29]

    post { [cite: 53, 54]
        always { [cite: 54]
            // This happens regardless of build success or failure [cite: 54]
            echo 'Post build condition running' [cite: 54]
        }
        failure { [cite: 54]
            // This happens only if the build fails [cite: 54]
            echo 'Post Action if Build Failed' [cite: 54]
        }
    }
} // <--- THIS must be the very last line [cite: 29]
