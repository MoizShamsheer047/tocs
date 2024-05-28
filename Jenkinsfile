pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        git url: 'https://github.com/MoizShamsheer047/tocs.git', branch: 'master'
      }
    }
    stage('Deploy Website') {
      steps {
        script {
          // Ensure the target directory exists and copy all project files
          sh '''
            gcloud compute ssh root@jenkinsserver --zone=us-west4-b --command="mkdir -p /var/www/html"
            gcloud compute scp --recurse /var/lib/jenkins/workspace/ASSIGNMENT_4_master/* root@jenkinsserver:/var/www/html --zone=us-west4-b
          '''
        }
      }
    }
    stage('Restart Apache') {
      steps {
        script {
          // Restart Apache to ensure the new files are served
          sh '''
            gcloud compute ssh root@jenkinsserver --zone=us-west4-b --command="sudo systemctl restart apache2"
          '''
        }
      }
    }
  }
}
