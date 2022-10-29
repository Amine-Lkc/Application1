pipeline {
    agent any
    tools {
        nodejs 'node 16'
    }
    stages {
        stage('build') {
            steps {
                sh 'cd client && npm install' 
            }
        }

        stage('testing') {
            steps {
                echo "testing...."
            }
        }
    }
}