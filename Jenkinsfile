pipeline {
    agent any

    environment {
        dockerHome = tool "myDocker"
        mavenHome = tool 'myMaven'
        PATH = "${dockerHome}/bin:${mavenHome}/bin:${env.PATH}"
    }

    stages{
        stage('Build'){
            sh 'mvn --version'
            sh 'docker --version'
        }
    }
}
