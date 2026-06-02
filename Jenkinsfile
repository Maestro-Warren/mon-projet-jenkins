  p
ipeline {
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
                  echo "Construction du build #${BUILD_NUMBER}"
                  sh 'cat README.md'
              }
          }
          stage('Test') {
              steps {
                  echo "Lancement des tests..."
                  sh 'test -f Jenkinsfile && echo "Jenkinsfile existe : OK"'
                  sh 'test -f README.md && echo "README existe : OK"'
              }
          }
          stage('Deploy') {
              steps {
                  echo "Deploiement termine !"
              }
          }
      }
  
      post {
          success {
              echo "Pipeline reussie !"
          }
          failure {
              echo "Pipeline echouee !"
          }
      }
  }
