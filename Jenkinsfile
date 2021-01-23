pipeline {
 
  agent {
        docker {
            image 'node:current-buster'
            args '-p 3000:3000'
        }
    }
 
  stages {
    stage('Example') {
      steps {
        sh 'npm config ls'
      }
    }
    stage('Cloning Git') {
      steps {
        git 'https://github.com/kanad13/test-node'
      }
    }
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
    stage('Cowsay') {
      steps {
        sh 'node index.js'
      }
    }
  }
}
