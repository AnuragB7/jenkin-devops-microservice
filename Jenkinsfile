// Declarative
pipeline {
	agent any
	// agent { docker {image 'maven:3.6.3'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Compile'){
			steps {
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				sh "mvn clean compile"
			}
		}
		stage('Test'){
			steps {
				echo "Test"
				sh "mvn test"
			}
		}
		stage('Integration Test'){
			steps {
				echo "Integration Test"
				sh "mvn failsafe:integration-test failsafe:verify"
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
