pipeline{
    agent any
    stages{
       
        stage("sonar quality check"){
         agent {
                docker {
                    image 'openjdk:11'
                }
            } 

          steps{
             withSonarQubeEnv(credentialsId: 'sonar-password') {
                sh 'chmod +x gradlew'
                sh './gradlew sonarqube'
              }
                
             }  
            
           
        }
    }
    
}