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
			input 'Do you approve deployment?'
			steps{
				ansiColor("xterm") {
					echo "Test..."
					sh 'ls -a'
				}
			}
		}
		stage('Online') {
			steps{
				ansiColor("xterm") {
					echo "Online"
					sh 'ls -a'
				}
			}
		}
	}
}
