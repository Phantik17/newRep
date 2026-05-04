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
                bat 'py -m pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'py -m pytest'
            }
        }
    }
}
