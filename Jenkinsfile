pipeline {
    agent any

    environment {
        dockerHome = tool "myDocker"
        mavenHome = tool 'myMaven'
        PATH = "${dockerHome}/bin:${mavenHome}/bin:${env.PATH}"
    }

    stages{
        stage('Build'){
            steps{
                sh "mvn clean compile"
            
        }}

        // stage('Test'){
        //     steps{
        //         sh "mvn test"
        //     }
        // }
        stage("Integration Test"){
            steps{
                sh "mvn failsafe:integration-test failsafe:verify"
            }
        }
    }
}
