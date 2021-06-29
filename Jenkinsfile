pipeline{
agent any
  stages{
    stage("build"){
      steps{
    echo "hello build"
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
        }
  }
  }
}
