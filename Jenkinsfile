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
                    sh '/var/lib/jenkins/.local/bin/pipenv run python3 manage.py test'
                }
            }
        }
        stage('Deploy-to-Staging') { 
            steps {
                sh 'ssh -o StrictHostKeyChecking=no deployment-user@192.168.56.107 "cd polling; \
                 git pull origin master; \
                 pipenv install; \
                 cd polling; \
                 pipenv run python3 manage.py migrate; \
                 sudo systemctl restart nginx; \
                 sudo systemctl restart gunicorn"'
            }
        }
        stage('Deploy-to-Prod') { 
            steps {
                sh 'ssh deployment-user@192.168.56.101 "cd polling; \
                 git pull origin master; \
                 pipenv install; \
                 cd polling; \
                 pipenv run python3 manage.py migrate; \
                 sudo systemctl restart nginx; \
                 sudo systemctl restart gunicorn"'
            }
        }
    }
}