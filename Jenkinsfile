pipeline {
  agent none

  stages {
    stage('error') {
          agent {
          docker {
            image 'ubuntu:latest'
          } //docker image
        } //end agent
      
        steps {
          sh 'echo "i am here"'
          sh 'cat  /etc/os-release'
        }
          
    } // end stage
    
    
  } // end stages
}
