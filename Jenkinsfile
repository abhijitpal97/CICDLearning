pipeline {
    agent any    

    stages {
        
        stage("SCM Checkout"){
            steps{
            git 'https://github.com/abhijitpal97/CICDLearning'
            }
        }   
            
        stage ('Compile Stage') {

            steps {   
                maven(maven : 'maven_3_8_5'){
                       bat 'mvn clean compile'                
                }
                 
            }
        }
        
        stage ('Testing Stage') {

            steps {
                maven(maven : 'maven_3_8_5'){
                    bat 'mvn test'
                }
                 
            }
        }


        stage ('Deployment Stage') {
            steps {
                maven(maven : 'maven_3_8_5'){
                    bat 'mvn deploy'
                }
                
            }
        }

    }
}
