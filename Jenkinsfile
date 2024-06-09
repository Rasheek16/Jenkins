pipeline {
	// agent {docker {image 'maven:3.6.3'}}
	stages{
		agent any
		environment {
			dockerHome = tool 'mydocker'
			mavenHome = tool 'myMaven'

			PATH="$dockerHome/bin:mavenHome/bin:$PATH"
					}
		stage('Build'){
			steps {
				// sh "mvn --version"
				echo "Build"
				echo "$PATH"
				sh 'mvn --version'
				ss 'docker --version'
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