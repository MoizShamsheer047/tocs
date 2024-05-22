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
        gcloud compute scp /var/lib/jenkins/workspace/ASSIGNMENT_4_master/index.html root@apacheserver:/var/www/html --zone=us-central1-a
      }
    }
  }
}
