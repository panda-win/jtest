pipeline {
	agent any
	parameters {
		choice(
			choices: ['test','pro'],
			description: '',
			name: 'RUN_MODE'
		)
	}
	stages {
		stage('StaticCheck') {
			steps{
				sh 'ls -a'
				sh 'echo $PWD'	
			}
		}
		stage('Build') {
			steps{
				sh 'echo $PWD'
			}
		}
		stage('Test') {
			steps{
				input message: 'Do you want to continue deployment?'
				echo "Test..."
			}
		}
		stage('Online') {
			steps{
				input message: 'Do you want to continue deployment?'
				echo "Online..."
				sh 'ls -a'
			}
		}
	}
}
