pipeline{
agent any
  environment{
    New_version="1.2.1"
  }
  stages{
    stage("build"){
      steps{
        echo "hello build version ${New_version}"
    }
    }
    stage("test"){
      when {
        expression{
        BRANCH_NAME=="master"
        }
      }
      steps{
        echo "hello test"
       /* withCredentials([usernamePassword(credentials: '', passwordVariable: '', usernameVariable: '')]) {
    // some block
}*/
        }
  }
  }
  
    
}
