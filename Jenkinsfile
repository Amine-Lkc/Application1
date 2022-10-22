pipeline {
    agent any
    
    stages {
        stage('build') {
            steps {
                sh 'cd client'
                sh 'npm install'
            }
        }

        stage('testing') {
            steps {
                echo "testing...."
            }
        }
    }
}