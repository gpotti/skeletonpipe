pipeline{ //beginning of pipeline
  agent any
 // parameters {
    //
 // }
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
    
    stage ('Test') {
     steps { //to add another stage in parallel, adding steps 
      parallel {
        stage ('Testing') {
          stages {
            stage ('Static Test') {
              steps{
                echo 'static test ON'
              } //step static test end
            } //stage static test end
            stage ('QA') {
                   steps{
                     echo 'QA ON'
                   } //step QA end
            } //stage QA end
          } //multiple stages end
          stage ('unit test') {
            steps {
              echo 'unit test in parallel ON'
            } //step unit test end
          } //stage unit test end
        } //Stage testing end
      } //end of parallel
     } //end of steps inside Test
    } //end of stage Test
      
      stage ('deploy') {
        steps {
          echo 'deploy something somewhere'
        } //end of deploy step
      } //end of deploy stage
      
    } //end of all stages 
  } //end of pipeline
              
