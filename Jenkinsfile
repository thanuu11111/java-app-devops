pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Build Jar package'
            }
        }
        stage('Test'){
            steps{
                echo 'running tests'
            }
        }    
        stage('Package'){
            steps{
                sh 'mvn clean package'
            }
        }    
        stage('Post-Build'){
            steps{
                echo 'Build successful..'
            }
        }
       // stage('Publish in Nexus repo'){
          //  steps{
          //      sh 'mvn deploy'//
          //  }
       // }
    }
}