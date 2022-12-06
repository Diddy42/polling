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
                dir("/var/lib/jenkins/workspace/polling-pipeline/polling"){
                    sh 'pwd'
                }
                sh 'pwd'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo deploying'
            }
        }
    }
}