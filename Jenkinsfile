pipeline {
    agent any 
    stages {
        stage('Rebuild dependencies') { 
            steps {
                bat 'dotnet restore' 
            }
        }
        stage('Rebuild application') { 
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Run tests') { 
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
