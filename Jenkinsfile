// Declarative
pipeline {
	agent any
	// agent { docker {image 'maven:3.6.3'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHomeHome/bin:$PATH"
	}
	stages{
		stage('Build'){
			steps {
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
			}
		}
		stage('Test'){
			steps {
				echo "Test"
				echo "Test"
			}
		}
		stage('Integration Test'){
			steps {
				echo "Integration Test"
			}
		}

	}

	post {

		always{

			echo "I run always"
		}
		success{

			echo "I run when you are successful "
		}
		failure{

			echo "I run when you fail"
		}


	}
	
}
