pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh '/var/lib/jenkins/.local/bin/pipenv install'
            }
        }
        stage('Test') { 
            steps {
                sh '/var/lib/jenkins/.local/bin/pipenv shell'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo deploying'
            }
        }
    }
}