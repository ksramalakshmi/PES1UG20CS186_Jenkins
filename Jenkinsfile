pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        g++ main2.cpp -o main2file
        build PES1UG20CS186-1
      }
    }
    
    stage('Test') {
      steps{
        ./main2file
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
    
      
