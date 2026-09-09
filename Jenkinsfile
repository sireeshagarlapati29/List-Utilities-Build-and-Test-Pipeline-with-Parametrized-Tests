pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/sireeshagarlapati29/List-Utilities-Build-and-Test-Pipeline-with-Parametrized-Tests.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat '"C:\\Program Files\\Python310\\python.exe" -m pip install -r requirements.txt'
            }
        }

        stage('Run Unit Tests') {
            steps {
                bat '"C:\\Program Files\\Python310\\python.exe" -m pytest test_app.py -v'
            }
        }
    }
}