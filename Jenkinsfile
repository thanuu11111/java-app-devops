pipeline{
    agent any
    stages{
        stage('Build'){
            step{
                echo 'Build Jar package'
            }
        }
        stage('Test'){
            step{
                echo 'running tests'
            }
        }    
        stage('Package'){
            step{
                sh 'mvn clean package'
            }
        }    
        stage('Post-Build'){
            step{
                echo 'Build successful..'
            }
        }
       // stage('Publish in Nexus repo'){
          //  step{
          //      sh 'mvn deploy'//
          //  }
       // }
    }
}