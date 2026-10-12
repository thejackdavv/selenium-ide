pipeline{
    agent any
    stages{
        stage("Restore the project"){
            steps{
                sh "dotnet restore"
            }
        }
        stage("Build the project"){
            steps{
                sh "dotnet build --no-restore"
            }
        }
        stage("Run unit tests"){
            steps{
                sh "dotnet test --no-build --verbosity normal"
            }
        }
    }
    
}