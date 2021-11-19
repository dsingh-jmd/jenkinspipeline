pipeline {
  agent any
  stages {
    stage('Find IP') {
      parallel {
        stage('Find IP') {
          steps {
            bat 'ipconfig'
          }
        }

        stage('Create and validate file') {
          steps {
            writeFile(file: 'config.conf', text: 'This is a configuration file for our application')
            fileExists 'config.conf'
          }
        }

      }
    }

    stage('Development') {
      steps {
        echo 'This step prints to development'
      }
    }

    stage('Test') {
      steps {
        echo 'This step prints to test'
      }
    }

    stage('Production') {
      steps {
        echo 'This step prints production'
      }
    }

  }
}