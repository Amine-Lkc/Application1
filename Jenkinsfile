pipeline {
    agent any
    
    environment {
        DOCKERHUB_CREDENTIALS = credentials('DockerJenkins')
        }
    stages {
        
        stage('build') {
            steps {
                sh 'cd client && docker build -t medaminelmk/front:front .' 
            }
        }
        stage('login') {
            steps {
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u medaminelmk' 
            }
        }

        stage('push') {
            steps {
                sh "docker push bahachalbia/front:front"
            }
        }
    }
}