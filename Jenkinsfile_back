def gvv
pipeline{
agent any
  environment{
    New_version="1.2.1"
  }
 parameters {
  string defaultValue: '1', description: 'used for testing', name: 'jenkins', trim: false
}
  stages{
    stage("init"){
      steps{
        script{
          gvv= load "test.groovy"
        }
      }
    }
    stage("build"){
      steps{
        echo "hello build version ${New_version}"
        echo "testing parameter ${params.jenkins}"
    }
    }
    stage("test"){
      when {
        expression{
        BRANCH_NAME=="main"
        }
      }
      steps{
        script{
         gvv.test()
        }
       /* withCredentials([usernamePassword(credentials: '', passwordVariable: '', usernameVariable: '')]) {
    // some block
}*/
        }
  }
  }
  
    
}
