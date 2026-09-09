ipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/<student-username>/<repo-name>.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Run Unit Tests') {
        steps {
                bat 'pytest test_app.py -v'
            }
        }
    }
}