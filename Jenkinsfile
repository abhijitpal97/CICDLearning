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
	    
	   stage('Sonarqube') {
    environment {
        scannerHome = tool 'SonarQubeScanner'
    }
    steps {
        withSonarQubeEnv('sonarqube') {
            sh "${scannerHome}/bin/sonar-scanner"
        }
        timeout(time: 10, unit: 'MINUTES') {
            waitForQualityGate abortPipeline: true
        }
    }
}

         stage('testing stage') {
             steps {
                bat "mvn test"
	     }
	 }
	    
	stage('email notification') {
             steps {
                mail bcc: '', body: '''Hi 
                Welcome to Jenkins alert services.''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job Update', to: 'abhijitpal97@yahoo.co.in'
	     }
	 }
  }

}
