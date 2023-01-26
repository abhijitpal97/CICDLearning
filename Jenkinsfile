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
		
        stage('Compile stage') {
            steps {
                bat "mvn clean compile" 
        }
    }

         stage('testing stage') {
             steps {
                bat "mvn test"
        }
    }

          stage('deployment stage') {
              steps {
                bat "mvn deploy"
        }
    }

  }

}
