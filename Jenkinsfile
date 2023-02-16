pipeline {
    agent any
    environment {
    DOCKERHUB_CREDENTIALS = credentials('dockerhubaccount')
  }
    stages{
        stage('Keerti - Build Docker Image'){
            steps {
                
                sh 'docker image build -t keertimaan/python-image .'
                
            }
        }
        stage('Keerti - Login to Dockerhub'){
            steps {
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
            }
        }
        stage('Keerti - Push image to Dockerhub'){
            steps{
                sh 'docker image push keertimaan/python-image'
            }
        }
    }
}