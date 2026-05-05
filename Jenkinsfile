pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }

    // This is the new section to add
    post {
        success {
            mail to: 'akashchittiappa100@gmail.com',
                 subject: "Build Successful: ${env.JOB_NAME} [${env.BUILD_NUMBER}]",
                 body: "Great news! The build was successful. Check it out here: ${env.BUILD_URL}"
        }
        failure {
            mail to: 'gopikagopal2005@gmail.com',
                 subject: "Build Failed: ${env.JOB_NAME} [${env.BUILD_NUMBER}]",
                 body: "The build failed. Review the logs at: ${env.BUILD_URL}console"
        }
    }
}
