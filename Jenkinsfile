pipeline {
  agent any

  stages {
    

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
