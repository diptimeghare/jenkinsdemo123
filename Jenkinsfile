pipeline{
    agent any
    environment{
        PYTHON='C:\\Users\\Win11\\AppData\\Local\\Programs\\Python\\Python313\\python.exe'
    }
    triggers{
        cron("*/2 * * * *")
    }
    stages{
        stage('Checkout code'){
            steps{
                checkout scm
            }
        }
        stage('Extarct data'){
            steps{
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