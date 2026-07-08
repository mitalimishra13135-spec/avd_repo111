pipeline{
    agent any
    environment{
        PYTHON = 'C:\\Users\\USER\\AppData\\Local\\Programs\\Python\\Python312\\python.exe'
    }
    stages{
        stage('checkout code'){
            steps{
                checkout scm      
            } 
        }

        stage('install dependencies'){
            steps{
                bat "${env.PYTHON} -m pip install -r requirements.txt"
            }
        }
        stage('run extract_data.py'){
            bat "${env.PYTHON} extract_data.py"
        }
    }
}