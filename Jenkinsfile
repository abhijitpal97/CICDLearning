node
{
    stage('SCM Checkout'){
        git('https://github.com/abhijitpal97/CICDLearning')
    }
    stage('Compile Package')
    {
        def mvnHome = tool name: 'maven_3_8_5', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
}
