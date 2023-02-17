pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        sh 'g++ woring.cpp'
        build job: "PES2UG20CS576-1", wait: true
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
      }
    }
  }
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
