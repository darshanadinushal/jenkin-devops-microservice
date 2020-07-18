pipeline {
    agent { 
		docker { 
			image 'maven:3.6.3'
			label 'docker'
		} 
	}
    stages {
        stage('Build') {
            steps {
                echo "Build"
            }
        }
    }
}