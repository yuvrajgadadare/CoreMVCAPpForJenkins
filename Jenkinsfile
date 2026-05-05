pipeline {
    agent any
    environment {
        DOTNET_CLI_HOME="C:\\Program Files\\dotnet"
    }
    stages {
        stage("Checkout") {
         steps {
               checkout scm
         }
        }
        stage("Build") {
            steps {
                bat "dotnet restore"
                bat "dotnet build --configuration Release"
            }
        }
        stage("Test") {
            steps {
                bat "dotnet test --no-restore --configuration Release"
            }

        }

    }

}