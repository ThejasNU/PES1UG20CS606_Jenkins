pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES1UG20CS606_test PES1UG20CS606_test.cpp'
        build job: 'PES1UG20CS606-1'
        echo 'Build stage done'
      }
    }
    stage('Test') {
      steps {
        sh './PES1UG20CS606_test'
        echo 'Test stage done'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed successfully!!'
      }
    }
  }
  
  post{
    failure{
        echo "Pipeline failed!!"
    }
  }
}
