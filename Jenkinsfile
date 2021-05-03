pipeline{ //beginning of pipeline

  agent any

  stages { //beginning of all stages
    stage ('Git pull'){
      steps {
        echo 'code pull from git'
      }
    } //git pull stage end
    
    stage ('check if build needed') {
      steps {
        echo 'http req etc and parse json'
      } 
    } //check build needed end
    
    stage ('build') {
      steps {
        echo 'do build stuff'
      }
    } //build stage end
    
    stage ('Parallel Test') {
      parallel {
        stage ('static test') {
          steps {
            echo 'static test'
          }//step static testend
        }//stage static test end
        stage ('Unit test') {
          steps {
            echo 'Unit test'
          }//step unit test end
        }//stage unit test end
      } //end of parallel
    }//end of stage parallel test
        
        
    
  } //end of all stages
} //end of pipeline
