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
				echo 'start static check'
			}
		}
		stage('Build') {
			steps{
				sh 'go build -o run main.go'
			}
		}
		stage('Test') {
			steps{
				input message: 'Do you want to continue deployment?'
				echo 'Test...'
				sh './run'
			}
		}
		stage('Online') {
			steps{
				input message: 'Do you want to continue deployment?'
				echo "Online..."
				sh './run'
			}
		}
	}
}
