pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // This uses the 'mvn' command installed on your OS
                sh 'mvn clean install'
            }
        }
    }
}
