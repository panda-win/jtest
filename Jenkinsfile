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
			steps{
				ansiColor("xterm") {
					sh 'echo $PWD'	
				}
			}
		}
		stage('Build') {
			steps{
				ansiColor("xterm") {
					sh 'echo $PWD'
					sh 'make build'
				}
			}
		}
		stage('Test') {
			steps{
				ansiColor("xterm") {
					sh 'ls -a'
				}
			}
		}
		stage('Online') {
			steps{
				ansiColor("xterm") {
					sh 'ls -a'
				}
			}
		}
	}
}
