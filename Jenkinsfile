pipeline {
  agent any

  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/namakamu/php-jenkins.git'
      }
    }

    stage('Build Docker') {
      steps {
        sh 'docker build -t php-jenkins .'
      }
    }

    stage('Run Docker') {
      steps {
        sh 'docker run -d -p 8082:80 php-jenkins'
      }
    }
  }
}
