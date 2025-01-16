pipeline {
    agent any
    stages{
        stage('build project'){
            steps{
                git url:'https://github.com/Nancy2209/star-agile-banking-finance/', branch: "master"
                sh 'mvn clean package'
              
            }
        }
        stage('Build docker image'){
            steps{
                script{
                    sh 'docker build -t Nancy2209/star-agile-banking-finance:v1 .'
                    sh 'docker images'
                }
            }
        }
         
        
     stage('Deploy') {
            steps {
                sh 'sudo docker run -itd --name My-first-containe21211 -p 8083:8081 aNancy2209/star-agile-banking-finance:v1'
                  
                }
            }
        
    }
}