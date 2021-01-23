pipeline {
  agent any
 
  //tools {nodejs "node"}
 
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
