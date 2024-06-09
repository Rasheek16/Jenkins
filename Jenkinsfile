pipeline {
	// agent {docker {image 'maven:3.6.3'}}
		agent any

		environment {
			dockerHome = tool "myDocker"
			mavenHome = tool "myMaven"
			PATH="$dockerHome/bin:mavenHome/bin:$PATH"
		}
	stages{
		stage('Build'){
			steps {
				// sh "mvn --version"
				echo "Build"
				echo "$PATH"
				sh "docker --version"
				sh "mvn --version"
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