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
          echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"

        }
                      post {
        always {
          sh 'echo "i am in post2"'
    
        }
      }
          
    } // end stage
    
    
    
  } // end stages
}
