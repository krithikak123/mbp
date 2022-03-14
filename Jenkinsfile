pipeline{
    agent any
    tools {
       maven 'maven3'
    }

    stages{
        stage("maven build"){
            when{
                branch 'develop'
            }
            steps{
                sh "mvn clean package"
            }
        }
        stage("sonar analysis"){
            when{
                branch 'develop'
            }
            steps{
               echo "sonar analysis"
            }
        }
        stage("upload to nexus"){
            when{
                branch 'develop'
            }
            steps{
                echo "uploading war file to nexus"
            }
        }
        stage("deploy to dev and test"){
            when{
                branch 'develop'
            }
            steps{
                echo "deploying to develop"
                echo "deploying to test"
            }
        }
        stage("UAT"){
            when{
                branch 'UAT'
            }
            steps{
                echo "deploying to UAT"
            }
        }
        stage("maven build"){
            when{
                branch 'master'
            }
            steps{
                echo "deploying to production"
            }
        }
    }
}