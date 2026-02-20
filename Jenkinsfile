pipeline{
    agent any

     triggers {
        githubPush()
    }

    stages{
        stage("Restore app"){
             when {
                branch 'main'
            }
            steps{
                bat "dotnet restore"
            }
        }
         stage("Build app"){
             when {
                branch 'main'
            }
            steps{
                bat "dotnet build"
            }
        }
         stage("Test app"){
             when {
                branch 'main'
            }
            steps{
                bat "dotnet test"
            }
        }
    }
}