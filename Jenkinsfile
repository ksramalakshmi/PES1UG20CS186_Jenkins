pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        g++ main2.cpp
        build PES1UG20CS186-1
      }
    }
    
    stage('Test') {
      steps{
        ./a.out
      }
    }
    
    stage('Deploy') {
      steps{
        sh 'mvn deploy'
        echo 'Deployment successful'
      }
    }
  }
  post{
    failure {
      echo 'Pipeline failed'
    }
  }
}
    
      
