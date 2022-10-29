pipeline {
    agent any
    
    environment {
        DOCKERHUB_CREDENTIALS = credentials('DockerJenkins')
        }
    stages {
        stage('CD') {
            steps {
                sh 'cd client' 
            }
        }
        stage('build') {
            steps {
                sh 'docker build -t medaminelmk/front:front .' 
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