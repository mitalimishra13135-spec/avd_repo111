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
        stage('show python version'){
            steps{
                bat "${env.PYTHON} --version"
                
            }
        }
        stage('run extract_data.py'){
            steps{
                bat "${env.PYTHON} extract_data.py"
            }
        }

    }
}