pipeline {
    agent { label 'JDK-17' }
    stages {
        stage(giturl) {
            steps {
               git url: 'https://github.com/GitpracticeDemo/RRR.git',
                   branch: 'main'
            }
        }
        stage(build) {
            steps{
                sh 'terraform init'
                sh 'terraform fmt'
                sh 'terraform validate'
                sh 'terraform apply --auto-approve'
            }
        }
    }
}