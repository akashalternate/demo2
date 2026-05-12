pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }

    post {
        success {
            emailext (
                subject: "SUCCESS: \${JOB_NAME} #\${BUILD_NUMBER}",
                body: "Build succeeded!\nCheck: \${BUILD_URL}",
                to: "akashchittiappa100@gmail.com"
            )
        }
        failure {
            emailext (
                subject: "FAILED: \${JOB_NAME} #\${BUILD_NUMBER}",
                body: "Build failed!\nCheck: \${BUILD_URL}",
                to: "akashchittiappa100@gmail.com"
            )
        }
    }
}
