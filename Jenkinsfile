pipeline {
	agent any
	stages {
		stage('test') {
			agent {
				docker { image "node:slim" }
			}
			steps {
				sh """
					npm --version
					node --version"
					npm install newman"
					newman --version"
					newman run --verbose test_collection.json"
				"""
			}
		}
	}
}
