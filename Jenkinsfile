pipeline {
  agent any
  
  stages{
    stage('Build'){
      steps{
        sh 'echo "Building Application..."'
      }
    }
    
    stage('Docker'){
      steps{
        withCredentials([usernamePassword(credentialsId: 'personal-docker-credentials', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD')]){
          sh 'echo ${DOCKER_USERNAME}'
        }
      }
    }
    
  }
}
