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
        script {
          // Ensure the target directory exists
          sh '''
            gcloud compute ssh root@jenkinsserver --zone=us-west4-b --command="mkdir -p /var/www/html"
            gcloud compute scp /var/lib/jenkins/workspace/ASSIGNMENT_4_master/index.html root@jenkinsserver:/var/www/html --zone=us-west4-b
          '''
        }
      }
    }
  }
}
