pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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
    
    // Add this new section right here at the bottom
    post {
        always {
            // this action will happen always regardless of the result of build
            echo "Post Build condition running"
        }
        failure {
            // this action will happen only if the build has failed
            echo 'Post action if Build Fails'
        }
    }
}
