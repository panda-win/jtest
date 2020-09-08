pipeline {
	agent any
	tools {
		go 'go-1.13'
	}
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
				sh 'echo $PWD'	
			}
		}
		stage('Build') {
			steps{
				sh 'echo $PWD'
				sh 'go build -o run main.go'
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
