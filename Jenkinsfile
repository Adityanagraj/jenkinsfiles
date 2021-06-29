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
  post{
    success{
      mail bcc: '', body: 'test done', cc: '', from: '', replyTo: '', subject: 'build done', to: 'aditya.nagraja1999@gmail.com'
    }
  }
    
}
