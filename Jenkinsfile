pipeline {
    agent any
    tools {
        maven 'Maven 3.x' // Ensure this matches the name in Global Tool Configuration
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
