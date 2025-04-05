pipeline {
    agent any

    environment {
        SONAR_SCANNER_HOME = 'C:\\sonar-scanner-5.0.1.3006-windows\\bin'
        SONAR_HOST_URL = 'http://localhost:9000'
        SONAR_PROJECT_KEY = 'Alinuur'
        SONAR_LOGIN = 'sqa_132ecb74fd664e84e15ee694eebf0a7f53109247'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/alinuuryare111/Jenkins.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('alinuuryare') {
                   bat 'C:\\sonar-scanner-5.0.1.3006-windows\\bin\\sonar-scanner -Dsonar.projectKey=Alinuur -Dsonar.sources=src -Dsonar.host.url=http://localhost:9000 -Dsonar.login=sqa_132ecb74fd664e84e15ee694eebf0a7f53109247'
                }
            }
        }
    }
}
