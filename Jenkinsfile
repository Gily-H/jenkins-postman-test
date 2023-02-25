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
				npm install newman
				sh "newman --version"
				newman run --verbose test_collection.json
			}
		}
	}
}
