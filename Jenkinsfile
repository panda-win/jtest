pipeline {
	agent none
	parameters {
		choice(
			choices: ['test','dev','pro'],
			description: '',
			name: 'RUN_MODE'
		)
	}

	stages {
		stage('StaticCheck') {
			sh 'echo $PWD'	
		}

		stage('Build') {
			sh 'echo $PWD'
			sh 'make build'
		}

		stage('Test') {
			sh 'ls -a'
		}

		stage('Online') {
			sh 'ls -a'	
		}
	}
}
