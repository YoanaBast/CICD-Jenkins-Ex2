pipeline {
    agent any

    stages {
        stage('Restore') {
            steps {
                sh 'dotnet restore HouseRentingSystem.sln'
            }
        }

        stage('Build') {
            steps {
                sh 'dotnet build HouseRentingSystem.sln --configuration Release --no-restore'
            }
        }

        stage('Test') {
            steps {
                sh 'dotnet test HouseRentingSystem.sln --configuration Release --no-build'
            }
        }
    }
}