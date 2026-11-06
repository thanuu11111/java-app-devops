pipeline {
    agent any

    tools {
        jdk 'java17'
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
                sh '/opt/apache-maven-3.9.10/bin/mvn -version'
                sh '/opt/apache-maven-3.9.10/bin/mvn clean package'
            }
        }
        stage('Publish to Nexus') {
            steps {
                sh 'mvn deploy'
            }
        }

        stage('Post-Build') {
            steps {
                echo 'Build successful..'
            }
        }
    }
}