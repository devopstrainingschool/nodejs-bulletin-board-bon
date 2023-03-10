pipeline {
  agent any
  stages {
    stage ("Docker build") {
      steps {
        dir('bulletin-board-app'){
        sh 'docker build -t devopstrainingschool/nodejs-jenkins:2023 .'
        }
      }
    }
  stage ("Docker push") {
      steps {
        
        withDockerRegistry([ credentialsId: "Docker_hub", url: "https://index.docker.io/v1/" ]) {
          sh "docker push devopstrainingschool/nodejs-jenkins:2023"
        }
        
      }
    }
  
  }
 





}
