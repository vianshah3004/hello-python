pipeline {
    agent any

    environment {
        APP_HOST = '13.207.186.117'
        APP_DIR = '/opt/hello-python'
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                    python3 -m pip install --user -r requirements.txt
                '''
            }
        }

        stage('Run Tests') {
            steps {
                sh '''
                    python3 -m unittest discover -s tests
                '''
            }
        }

        stage('SonarQube Analysis') {
            steps {
                echo 'SonarQube analysis will be configured in Jenkins'
            }
        }

        stage('Deploy to App EC2') {
            steps {
                echo 'Deployment to App EC2 will be configured next'
            }
        }
    }
}
