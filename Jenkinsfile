pipeline {
    agent any
    stages{
        stage("Keerti - Build Docker Image"){
            sh "docker image build ."
        }
        stage("Keerti - Login to Dockerhub"){
            sh "Docker login"
        }
        stage("Keerti - Push image to Dockerhub"){
            sh "Docker image push keertimaan/python-image"
        }
    }
}