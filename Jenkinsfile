pipeline {
    agent any
    environment {
        PYTHON = 'C:\\Users\\admin\\AppData\\Local\\Programs\\Python\\Python313\\python.exe'
    }
    trigger {
        cron ("*/2 * * * *")
    }
    stages {
        stage('Checkout code') {
            steps {
                checkout scm

            }
            

        }
        stage('Extract Data') {
            steps {
                bat "${env.PYTHON} extract_data.py"

            }
            

        }
    }
    post {
        success {
            echo "Success..........."

        }
        failure {
            echo "Failure......."
        }
        always {
            echo "Always........"

        }
    }
}
