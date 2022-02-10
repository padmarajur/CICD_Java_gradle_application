pipeline{
    agent any
    stages{
       
        stage("sonar quality check"){
         agent {
                docker {
                    image 'openJDK:11'
                }
            } 

          steps{
             withSonarQubeEnv(credentialsId: 'Sonar_token') {
                  sh 'chmod +x gradlew'
                  sh './gradlew sonarqube'
                    
                } 
                
             }  
            
           
        }
    }
    
}