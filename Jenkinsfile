pipeline {
  agent none

  stages {
    stage('ubuntu release') {
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
    
    
        stage('rhel release') {
          agent {
          docker {
            image 'alpine:latest'
          } //docker image
        } //end agent
      
        steps {
          sh 'echo "i am here"'
          sh 'cat  /etc/os-release'
        }
          
    } // end stage
    
    
    
  } // end stages
}
