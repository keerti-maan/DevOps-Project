pipeline {
    agent any
    stages{
        stage('Keerti - Build Docker Image'){
            steps {
                
                sh 'docker image build -t python-image .'
                
            }
        }
        stage('Keerti - Login to Dockerhub'){
            steps {
                withCredentials([string(credentialsId: 'dockerhubaccount', variable: 'dockerhubpwd')]){
                sh 'docker login -u keertimaan -p ${dockerhubpwd}'
                }
            }
        }
        stage('Keerti - Push image to Dockerhub'){
            steps{
                sh 'docker image push keertimaan/python-image'
            }
        }
    }
}