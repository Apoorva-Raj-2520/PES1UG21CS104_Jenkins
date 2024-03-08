pipeline{
  agent any 
  stages{
    stage('Build'){
      steps{
        build 'PES1UG21CS104-1'
        sh 'g++ main.cpp -o output'
        echo 'Build Stage successsful'
      }
    }
    stage('Test'){
      steps{
        sh './output'
        echo 'Test Stage successsful'
        post{
          always{
            junit 'target/sunfire-reports/*xml'
          }
        }
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deployment successsful'
      }
    }
  }
  post{
    failure{
      echo 'Pipeline Failed'
    }
  }
}
