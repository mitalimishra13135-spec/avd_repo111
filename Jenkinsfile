pipeline{
    agent any
    environment{
        PYTHON = 'C:\\Users\\USER\\AppData\\Local\\Programs\\Python\\Python312\\python.exe'
        DB_PASSWORD = credentials('DB_PASSWORD')
    }
    stages{
        stage('checkout code'){
            steps{
                checkout scm      
            } 
        }

        stage('run extract_data.py'){
            steps{
                 bat """
                        set DB_PASSWORD1 = ${env.DB_PASSWORD}
                        ${env.PYTHON} extract_data.py
                     """
            }
        }
    }
}