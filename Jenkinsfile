pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            def mvnHome = tool name: 'maven_3_8_5', type: 'maven'
			sh "${mvnHome}/bin/mvn package"
        }
		
		stage ('Testing Stage') {

            def mvnHome = tool name: 'maven_3_8_5', type: 'maven'
			sh "${mvnHome}/bin/mvn test"
        }


        stage ('Deployment Stage') {
            def mvnHome = tool name: 'maven_3_8_5', type: 'maven'
			sh "${mvnHome}/bin/mvn deploy"
        }

    }
}
