pipeline {
    agent any
    stages {
        stage("Clone Code from the Repo"){
			steps{
			    git branch: 'main', url: 'https://github.com/kengnemar/nodejs-demo-app'
			}
		}
        stage('Install the node dependencies') { 
            steps {
                sh 'npm install' 
            }
        }
         stage('Test the node code') { 
            steps {
                sh './scripts/test.sh' 
            }
        }
        stage('Package the node code') { 
            steps {
                sh 'npm package' 
            }
        }
    }
}