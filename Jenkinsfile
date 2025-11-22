pipeline {
    agent any

    tools {
        nodejs "node"    // Jenkins NodeJS tool name
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/eshuramgarhia/aukhakamm.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Run Application') {
            steps {
                sh 'npm start'
            }
        }
    }
}
