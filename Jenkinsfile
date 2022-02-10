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
             withSonarQubeEnv(credentialsId: 'sonar-password') {
              
              }
                
             }  
            
           
        }
    }
    
}