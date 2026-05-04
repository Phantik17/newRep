pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Phantik17/newRep', branch: 'main'
            }
        }
        stage('Diagnostics') {
            steps {
                // Показываем версию Python и путь к нему
                bat 'C:\\Users\\miran\\AppData\\Local\\Programs\\Python\\Python311\\python.exe --version'
                // Проверяем наличие pip
                bat 'C:\\Users\\miran\\AppData\\Local\\Programs\\Python\\Python311\\python.exe -m pip --version'
                // Пробуем установить зависимости с подробным выводом
                bat 'C:\\Users\\miran\\AppData\\Local\\Programs\\Python\\Python311\\python.exe -m pip install --trusted-host pypi.org --trusted-host files.pythonhosted.org -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'C:\\Users\\miran\\AppData\\Local\\Programs\\Python\\Python311\\python.exe -m pytest'
            }
        }
    }
}
