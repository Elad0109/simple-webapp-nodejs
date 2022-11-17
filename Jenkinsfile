pipeline {
    agent any

    stages {
        stage('cleanWs') {
            steps {
                cleanWs()
            }
        }
        stage('pull') {
            steps {
                git 'https://github.com/pazifargan/simple-webapp-nodejs.git'
            }
        }
        stage('build') {
            steps {
                nodejs('nodejs8') {
                    sh 'npm install'
                }
            }
        }
        stage('test') {
            steps {
                nodejs('nodejs8') {
                    sh 'npm test'
                }
            }
        }
    }
}
