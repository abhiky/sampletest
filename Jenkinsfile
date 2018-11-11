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
          

            post {
        always {
          sh 'echo "i am in post1"'
        }
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
                      post {
        always {
          sh 'echo "i am in post2"'
          sh 'echo "i am in ${env.BRANCH_NAME}"'
          sh 'echo "i am using ${currentBuild.number}"'
        }
      }
          
    } // end stage
    
    
    
  } // end stages
}
