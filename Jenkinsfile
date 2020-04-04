// Declarative
pipeline {
	agent any
	stages{
		stage('Build'){
			steps {
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

		alwyas{

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
