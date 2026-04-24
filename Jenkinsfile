pipeline {
    agent any
    
    // 1. Add the parameters block here
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run test stage?')
    }
    
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
                bat 'mvn --version'
            }
        }
        
        stage('Test') {
            // 2. Add the 'when' condition here
            when {
                expression { params.executeTests }
            }
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
