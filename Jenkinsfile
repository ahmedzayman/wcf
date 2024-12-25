pipeline {
    agent any 

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/ahmedzayman/wcf' 
            }
        }
        stage('Build') {
            steps {
                bat 'dotnet build ./Solution1/Solution1.sln' 
                bat 'dotnet build ./RESTApi/RESTApi.sln' 
            }
        }
        stage('Test') { 
            // Add your test commands here
            // Example:
            // steps {
            //     sh 'dotnet test ./Solution1/Solution1.TestProject/Solution1.TestProject.csproj'
            //     sh 'dotnet test ./RESTApi/RESTApi.TestProject/RESTApi.TestProject.csproj'
            // }
        }
        stage('Deploy') {
            // Add your deployment commands here
            // Example:
            // steps {
            //     // Deploy Solution1
            //     sh 'dotnet publish ./Solution1/Solution1.sln -c Release -o ./Solution1/publish'
            //     // Deploy RESTApi
            //     sh 'dotnet publish ./RESTApi/RESTApi.sln -c Release -o ./RESTApi/publish'
            // }
        }
    }
}