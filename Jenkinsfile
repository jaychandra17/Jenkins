pipeline {
	agent {  label 'linux-node' }
	stages {
		stage('---clean----'){
			tools {
				maven 'maven_3.9.8'
			}
			steps {
				sh 'mvn --version'
				sh "mvn clean"
			}
		}
		stage('---test---') {
			tools {
				maven 'maven_3.9.0'
			}
			steps {
				sh 'mvn --version'
				sh "mvn test"
			}
		}
		stage('---package---'){
			tools {
				maven 'maven_3.8.1'
			}
			
			steps {
				sh 'mvn --version'
				sh "mvn package"
			}
		}
	}
	post {
		success {
			echo 'job was built successfully'
		}
		failure {
			echo 'job was not build..it was failed'
		}
	}
}
