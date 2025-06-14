pipeline{
    agent any

    stages{
        stage("Build the project"){
            steps{
                echo "executing bat command dotnet build"
                bat "dotnet build"
            }
        }
        
        stage("Run test #1"){
            steps{
                echo "executing bat command dotnet TestProject1"
                bat "dotnet test TestProject1"
            }
        }
        
        stage("Run test #2"){
            steps{
                echo "executing bat command dotnet TestProject2"
                bat "dotnet test TestProject2"
            }
        }
        stage("Run test #3"){
            steps{
                echo "executing bat command dotnet TestProject3"
                bat "dotnet test TestProject3"
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