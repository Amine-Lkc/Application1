pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                sh cd clients
                sh npm install
            }
        }

        stage('testing') {
            steps {
                echo "testing...."
            }
        }
    }
}