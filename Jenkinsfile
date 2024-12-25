pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'dotnet build ./Solution1/Solution1.sln'
                bat 'dotnet build ./RESTApi/RESTApi.sln'
                bat 'dotnet build ./gRPC/GrpcService/GrpcService.sln'
            }
        }
        stage('Test') {
            steps {
                bat "dotnet test ./Solution1/Solution1.sln" 
                bat "dotnet test ./RESTApi/RESTApi.sln"
                bat "dotnet test ./gRPC/GrpcService/GrpcService.sln"
            }
        }
        stage('Docker Build') {
            steps {
                bat 'docker-compose build'
            }
        }
        stage('Deploy') {
            steps {
                bat 'docker-compose up -d'
            }
        }
    }
}