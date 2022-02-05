pipeline{
   
    agent any     
    stages{
        stage("Sonarqube quality check"){
            agent {
                docker {
                    image 'openjdk:11'
                    }
                }
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar-token1') {
                      sh 'chmod +x gradlew'
                      sh './gradlew sonarqube'
                    }
                }
            }
            
            
        }
    }
    
}