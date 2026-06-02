 pipeline {
      agent any

      stages {
          stage('Checkout') {
              steps {
                  echo "Code recupere depuis Git"
                  sh 'ls -la'
              }
          }
          stage('Build') {
              steps {
                  echo "Construction du build"
                  sh 'cat README.md'
              }
          }
          stage('Test') {
              steps {
                  echo "Lancement des tests"
                  sh 'test -f Jenkinsfile && echo "Jenkinsfile existe"'
                  sh 'test -f README.md && echo "README existe"'
              }
          }
          stage('Deploy') {
              steps {
                  echo "Deploiement termine"
              }
          }
      }
  }
