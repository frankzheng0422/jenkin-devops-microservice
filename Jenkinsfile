
//Scripted
/*
node {
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Integration Test') {
		echo "Integration Test"
	}
}
*/
//Declarative
pipeline {
	//agent any
	agent { docker { image 'maven:3.6.3' } }
	stages {
		stage('Build') {
			steps {
				echo "mvn --version"
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	} 
	post {
		always {
			echo "This will always run"
		}
		success {
			echo "This will run only if successful"
		}
		failure {
			echo "This will run only if failed"
		}
		unstable {
			echo "This will run only if the run was marked as unstable"
		}
		changed {
			echo "This will run only if the state of the Pipeline has changed"
			echo "For example, if the Pipeline was previously failing but is now successful"
		}
	}
}