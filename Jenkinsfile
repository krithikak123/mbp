pipeline{
    agent any
    stages{
        stage("maven build"){
            when{
                branch 'develop'
            }
            steps{
                sh "mvn clean package"
            }
        }
    }
}