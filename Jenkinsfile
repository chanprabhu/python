pipleline {
   agent none
stages{
      stage('SCM Checkout'){
          agent {
            docker{
                git credentialsId: 'GIT_CREDENTIALS', url:https://github.com/peddoju23/myproject.git',branch: 'master'
                }
                  }
                           }
      stage('Build') {
         agent {
              docker{
                 image 'python:2-alpine'
                    }
                } 
          steps {
            sh 'python -m py_compile source/add2vals.py source/calc.py'
            stash(name:'compiled-result',includes: 'sources/*.py*')
                }
                    } 
      }
           }

                    


