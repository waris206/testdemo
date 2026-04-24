pipeline {
    agent any
    
    // 1. Add the environment block here
    environment {
        NEW_VERSION = '1.3.0'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
                // 2. Output the value of the variable
                echo "Building version ${NEW_VERSION}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    
    post {
        always {
            echo "Post Build condition running"
        }
        failure {
            echo 'Post action if Build Fails'
        }
    }
}
