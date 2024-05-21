pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/MoizShamsheer047/tocs.git', branch: 'master'
            }
        }
        stage('Run Python Script') {
            steps {
                sh 'script.py'
            }
        }
    }
}
