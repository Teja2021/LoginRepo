

node{
    stage('SCM Checkout'){
     
        git 'https://github.com/Teja2021/LoginRepo.git'
    }
    stage('Compile-Package'){
          def mvnHome= tool name: 'Maven 3.9.3', type: 'maven'
        sh "${mvHome}/bin/mvn package"
    }
}
