pipeline{
    agent {
        label 'slave-helm'
    }
    stages{
        stage("1"){
            steps{
                git branch: 'main', url: 'https://github.com/Adityanagraj/jenkinsfiles'
                sh 'mkdir /home/aditya_n/helm'
                sh 'mv myweb /home/aditya_n/helm'
                
                
            }
        }
        stage("2"){
            steps{
                sh 'helm upgrade myweb /home/aditya_n/helm/myweb'
            }
        }
    }
}
