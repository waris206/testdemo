pipeline {
    agent any
    
    // 1. Add the tools block here
    tools {
        maven 'Maven'
    }
    
    environment {
        NEW_VERSION = '1.3.0'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
                echo "Building version ${NEW_VERSION}"
                
                // 2. Add the tool command for Windows
                bat 'mvn --version' 
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
