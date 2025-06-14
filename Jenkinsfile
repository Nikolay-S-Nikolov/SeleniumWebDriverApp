pipeline{
    agent any

    stages{
        stage("Build the project"){
            steps{
                echo "executing bat command dotnet build"
                bat "dotnet build"
            }
            }
        
        stage("Test the project"){
            steps{
                echo "executing bat command dotnet test"
                bat "dotnet test"
            }
        }
    }

    post{
        always{
            echo "Pipeline execution completed"
        }
        success{
            echo "Build and test stages completed successfully"
        }
        failure{
            echo "Build or test stage failed"
        }
    }
}