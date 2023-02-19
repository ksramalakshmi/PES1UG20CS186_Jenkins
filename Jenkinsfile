pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh "make -C main"
                echo 'Build stage completed'
      }
    }
    
    stage('Test') {
      steps{
         sh "/var/jenkins_home/workspace/PES1UG20CS186/main/hello_exec"
         echo 'Testing stage completed'
      }
    }
  }
  post{
    failure {
      echo 'Pipeline failed'
    }
  }
}
    
      
