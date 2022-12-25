pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/prasanthghub/html-repo.git', branch: 'main', poll: true)
      }
    }

    stage('Inatall apache') {
      steps {
        sh '''sudo apt-get install apache2
'''
      }
    }

    stage('deploy app') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}