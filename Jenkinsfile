pipeline {
    agent any
    stages {
        stage("Clone Code from the Repo"){
			steps{
			    git branch: 'main', url: 'https://github.com/kengnemar/nodejs-demo-app'
			}
		}
        stage('Package the node code') { 
            steps {
                sh 'npm install' 
            }
        }
         stage('Test the node code') { 
            steps {
                sh 'npm test' 
            }
        }
        stage('Package the node code') { 
            steps {
                sh 'npm package' 
            }
        }
    }
}