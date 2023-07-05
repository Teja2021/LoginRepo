

pipeline {

    agent any


    stages {

        stage('Checkout') {

            steps {

                git 'https://github.com/Teja2021/LoginRepo.git'

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
