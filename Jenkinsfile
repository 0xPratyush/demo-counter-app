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

        
        
        
        
        }

}