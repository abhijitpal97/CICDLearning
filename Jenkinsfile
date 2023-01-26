pipeline {

    agent any
    tools {
        maven 'maven_3_8_5' 
    }
    stages {
	
		
        stage('Compile stage') {
            steps {
                bat "mvn package" 
        }
    }

         stage('testing stage') {
             steps {
                bat "mvn test"
        }
    }
  }

}
