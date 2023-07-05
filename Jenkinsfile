node{
    stage('Checkout'){
        git branch: 'master' , url:'https://github.com/Teja2021/LoginRepo.git'
    }
    stage('Build'){
        withMaven(maven : 'M3'){
            bat 'mvn compile'
        }
    }
}
pipeline{
    agent any
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch:'master',url:'https://github.com/Teja2021/LoginRepo.git'
            }
        }
        stage('Build'){
            steps{
                bat 'mvn compile'
            }
        }
        stage('Test'){
            steps{
                bat 'mvn test'
            }
        }
        stage('Package'){
            steps{
                bat 'mvn package'
            }
        }
        stage('Deploy'){
            steps{
                echo 'deployed...'
            }
        }  
    }
}
