pipeline {
    agent any
     tools {
        git '<git-installation>'
    }

    stages {
        stage('Checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/Teja2021/LoginRepo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Deploy') {
            steps {
                sh 'mvn deploy'
            }
        }
    }
}

has context menu
