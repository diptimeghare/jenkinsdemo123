pipeline{
    agent any
    environment{
        PYTHON='C:\\Users\\Win11\\AppData\\Local\\Programs\\Python\\Python313\\python.exe'
    }
    stages{
        stage('Checkout code'){
            step{
                checkout scm
            }
        }
        stage('Extarct data'){
            step{
                bat "$env.PYTHON extract.py"
            }
        }
    }
    post{
        success{
            echo "Success...."
        }
        failure{
            echo "failure..."
        }
        always{
            echo "always..."
        }
    }
}