pipeline {
	agent any
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
				}
			}
		}
		stage('Test') {
			steps{
				input message: 'Do you want to continue deployment?'
				ansiColor("xterm") {
					echo "Test..."
					sh 'ls -a'
				}
			}
		}
		stage('Online') {
			steps{
				input message: 'Do you want to continue deployment?'
				ansiColor("xterm") {
					echo "Online"
					sh 'ls -a'
				}
			}
		}
	}
}
