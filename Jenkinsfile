pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
        stage('List Directory Contents') {
            steps {
                sh 'ls -la'
            }
        }
        stage('Run Python Script') {
            steps {
                sh 'python3 script.py'  // Update this path if your script is in a subdirectory
            }
        }
    }
}
