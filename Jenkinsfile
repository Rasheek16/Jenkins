pipeline {
	agent {docker {image 'maven:3.6.3'}}
	stages{
		stage('Build'){
			steps {
				sh "mvn --version"
				echo "Build"
			}
		}
		stage('Test'){
			steps {
			
				echo "Test"
			
			}
		}
		stage('Integration'){
			steps {
			
				echo "Integration"
			}
		}
	}
	post{
		always{
			echo "always"
		}
		success {
			echo "success"
		}
		failure{
			echo "failure"
		}
	}
}