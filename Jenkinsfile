pipeline{
	agent { 
		none
	}
	stages{
		stage('Build'){

			agent {
                docker { image 'maven:3-alpine' }
            }

			steps{
				sh 'mvn --version'
				echo "Build"
			}
		}

		stage('Test'){

			agent {
                docker { image 'node:7-alpine' }
            }
			steps{
				sh 'node --version'
				echo "Test"
			}
		}

		stage('Integration'){
			steps{
				echo "Integration"
			}
		}

	}

	post{
		always {
			echo "I'm awesome ,I run always"
		}

		success {
			echo "I run when you are successful"
		}

		failure {
			echo "I run when you fail"
		}
	}
}