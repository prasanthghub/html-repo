pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/prasanthghub/html-repo.git', branch: 'main', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('deployapp') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}