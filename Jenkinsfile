pipeline{
    agent any
    stages{
        stage("Checkout the code"){
            steps{
                echo "Checking out the code..."
                git branch: "main", url: "https://github.com/mixailvelinov/SeleniumIDE-EX"
            }
        }

        stage("Set up .NET Core"){
            steps{
                echo "Setting up .NET Core..."
                bat "choco install dotnet-sdk"
            }
        }

        stage("Restore dependencies"){
            steps{
                echo "Restoring dependencies..."
                bat "dotnet restore"
            }
        }

        stage("Build app"){
            steps{
                echo "Building app..."
                bat "dotnet build"
            }
        }

        stage("Run the tests"){
            steps{
                echo "Running the tests..."
                bat "dotnet test"
            }
        }
  }
}
