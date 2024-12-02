pipeline{

    agent any

    stages{

        stage("Git checkout"){

            steps{
                git branch: 'main', url: 'https://github.com/0xPratyush/demo-counter-app.git'
            }
        }

         stage("Unit Testing"){

            steps{
                sh 'mvn test'
            }
            
        }

         stage("Integration testing"){

            steps{
                sh 'mvn verify -DskipUnitTests'
            }
            
        }

        stage("Maven Build"){

            steps{
                sh 'mvn clean install'
            }
            
        }

         stage("SonarQube analysis"){

            steps{
                script{
              withSonarQubeEnv(credentialsId: 'sonarapi') {
                    sh 'mvn clean package sonar:sonar'
                                }         
                    }
            
        }

        
        
        
        
        }

}