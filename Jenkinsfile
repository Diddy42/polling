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
                echo 'testing'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo deploying'
            }
        }
    }
}