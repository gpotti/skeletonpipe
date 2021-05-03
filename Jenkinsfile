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
    
  } //end of all stages
} //end of pipeline
