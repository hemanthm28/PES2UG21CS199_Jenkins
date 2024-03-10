pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ main/hell3o.cpp -o run'
        echo 'Successfully compiled hello'
      }
    }
    stage('Test'){
      steps{
        sh './run'
      }
    }
    stage('Deploy'){
      steps{
        echo "Deployed" 
      }
    }
  }

  post{
    failure{
      echo "Pipeline Failed!"
    }
  }
}
