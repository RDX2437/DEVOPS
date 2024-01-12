pipeline {
    agent any

    environment {
        BUILD_LOGS = ''  // Initialize the variable here
    }
    stages {
        stage('Source') {
            steps {
                echo 'Hello, Mynotesoracledba Jenkins pipeline demo'
                git branch: 'Master', credentialsId: '66b19a99-ffb9-4f4e-a250-055dc13f982f', url: 'https://github.com/Mynotesoracledba/SampleJenkinsproject.git'
                sh 'cat web_scrapper.py'
            }
        }
        stage('Version') {
            steps {
                echo 'Check the Python version'
                sh 'python3 --version'
            }
        }
        stage('Build') {
           steps {
                echo 'Build Demo'
                sh 'pip install -r requirement.txt'
            }
        }
    
         stage('Deploy') {
           steps {
                echo 'Depoly Demo From 2-Tier'
                sh 'python3 web_scrapper.py'
            }
        }

    }
