pipeline {
    agent any

    tools {
        jdk 'java17'
    }

    environment {
        PATH+MAVEN = '/opt/apache-maven-3.9.10/bin'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build Jar package'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
            }
        }

        stage('Package') {
            steps {
                sh 'java -version'
                sh 'mvn -version'
                sh 'mvn clean package'
            }
        }

        stage('Post-Build') {
            steps {
                echo 'Build successful..'
            }
        }
    }
}