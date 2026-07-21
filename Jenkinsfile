pipeline{
    agent any
    stages{
        stage("Dotnet restore"){
            when {
                anyOf {
                    branch 'main'
                }
            }
            steps{
                bat "dotnet restore"
            }
            
        }
        stage("Dotnet build"){
            when {
                anyOf {
                    branch 'main'
                }
            }
            steps{
                bat "dotnet build --no-restore"
            }
        }
        stage("Dotnet run"){
            when {
                anyOf {
                    branch 'main'
                }
            }
            steps{
                bat "dotnet test --no-build --verbosity normal"
            }
        }
    }
}