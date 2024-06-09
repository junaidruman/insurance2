
pipeline {
    agent any
    stages{
        stage('build project'){
            steps{
                git url:'https://github.com/junaidruman/insurance/', branch: "master"
                sh 'mvn clean package'
              
            }
        }
        stage('Build docker image'){
            steps{
                script{
                    sh 'docker build -t junaidrumankhan/staragileprojectinsurance:v1 .'
                    sh 'docker images'
                }
            }
        }
         
        
     stage('Deploy') {
            steps {
                sh 'sudo docker run -itd --name My-second-containe21211 -p 8085:8081 junaidrumankhan/staragileprojectinsurance:v1'
                  
                }
            }
        
    }
}
