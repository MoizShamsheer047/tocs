pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from GitHub
                git url: 'https://github.com/MoizShamsheer047/tocs.git', branch: 'main'
            }
        }
        stage('Run Python Script') {
            steps {
                // Execute the Python script
                sh 'python3 script.py'
            }
        }
    }
}
