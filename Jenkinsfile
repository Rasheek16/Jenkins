pipeline {
    agent any

    environment {
        dockerHome = tool "myDocker"
        mavenHome = tool name: 'myMaven'
        PATH = "${dockerHome}/bin:${mavenHome}/bin:${env.PATH}"
    }

    stages {
        stage('Compile') {
            steps {
             sh "mvn clean compile"   
            }
        }

        stage('Test') {
            steps {
                sh "mvn test"
                // Add your test commands here
            }
        }

        stage('Integration') {
            steps {
               sh "mvn failsafe:integration-test failsafe:verify"
                // Add your integration test commands here
            }
        }
    }

    post {
        always {
            echo "always"
        }
        success {
            echo "success"
        }
        failure {
            echo "failure"
        }
    }
}
