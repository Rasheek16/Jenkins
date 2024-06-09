pipeline {
    agent any

    environment {
        dockerHome = tool name: 'myDocker', type: 'DockerTool'
        mavenHome = tool name: 'myMaven'
        PATH = "${dockerHome}/bin:${mavenHome}/bin:${env.PATH}"
    }

    stages {
        stage('Build') {
            steps {
                echo "Build"
                echo "${env.PATH}"
                sh "docker --version"
                sh "mvn --version"
            }
        }

        stage('Test') {
            steps {
                echo "Test"
                // Add your test commands here
            }
        }

        stage('Integration') {
            steps {
                echo "Integration"
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
