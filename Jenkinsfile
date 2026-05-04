pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Phantik17/newRep', branch: 'main'
            }
        }
        stage('Install') {
            steps {
                bat 'C:\\Users\\miran\\AppData\\Local\\Programs\\Python\\Python313\\python.exe -m pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'C:\\Users\\miran\\AppData\\Local\\Programs\\Python\\Python313\\python.exe -m pytest'
            }
        }
    }
}
