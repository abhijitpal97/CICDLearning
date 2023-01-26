pipeline {
    agent any
    tools {
        maven 'maven_3_8_5' 
    }

    stages {
        stage ('Compile Stage') {

            steps {                
                    sh 'mvn clean compile'                
            }
        }

    }
}
