pipeline {
  agent any
  stages{
    stage('Nginx intsalling'){
      steps{
        sh 'sudo apt install nginx -y'
      }
    }
    
    stage('Deleting Default'){
      steps{
        sh 'sudo rm rf /var/www/html/*'
      }
    }
    stage('Hosting'){
      steps{
        sh 'sudo cp rf /var/lib/jenkins/workspace/nginx/* /var/www/html/'
      }
    }
    stage('Restarting nginx'){
      steps{
        sh 'sudo systemctl resart nginx'
      }
    }
  }
}

