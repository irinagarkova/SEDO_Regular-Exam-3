pipeline {
    agent any
   
    stages {
        stage('Restore .Net Packages') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build .Net Project') {
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Run Tests') {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}