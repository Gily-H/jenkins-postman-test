pipeline {
	agent any
	stages {
		stage('test') {
			agent {
				docker { image "alpine:latest" }
			}
			steps {
				sh "npm --version"
				sh "node --version"
				sh "npm install newman"
				sh "newman --version"
				sh "newman run --verbose test_collection.json"
			}
		}
	}
}
