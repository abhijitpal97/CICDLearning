pipeline {
    agent any
    tools {
        maven 'maven_3_8_5' 
    }

    stages {
        
        stage("SCM Checkout"){
            steps{
            git 'https://github.com/abhijitpal97/CICDLearning'
            }
        }   
            
        stage ('Compile Stage') {

            steps {                
                    bat 'mvn clean compile'                
            }
        }
        
        stage ('Testing Stage') {

            steps {
                 bat 'mvn test'
            }
        }


        stage ('Deployment Stage') {
            steps {
                bat 'mvn deploy'
            }
        }

    }
}
