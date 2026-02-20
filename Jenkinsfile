pipeline{
    agent any

    stages{
        stage("Restore app"){
             when {
                expression { env.BRANCH_NAME == 'origin/main' }
            }
            steps{
                bat "dotnet restore"
            }
        }
         stage("Build app"){
            when {
                expression { env.BRANCH_NAME == 'origin/main' }
            }
            steps{
                bat "dotnet build"
            }
        }
         stage("Test app"){
             when {
                expression { env.BRANCH_NAME == 'origin/main' }
            }
            steps{
                bat "dotnet test"
            }
        }
    }
}