pipeline {
  agent any
  
  stages{
    stage('Test'){
      steps{
        sh 'echo "Running tests…"'
      }
    }
    
    stage('Build'){
      steps{
        sh 'echo "Building Application..."'
      }
    }
    
    stage('Docker'){
      steps{
        script {
          def dockerTool = tool name: 'docker-latest-tool', type: 'org.jenkinsci.plugins.docker.commons.tools.DockerTool'
          env.PATH = "${dockerTool}/bin:${env.PATH}"
        }
        sh "docker --version"
      }
    }
    
    stage('Deploy'){
      steps{
        sh 'echo "Deploying application to EC2 instance…"'
      }
    }
    
  }
}
