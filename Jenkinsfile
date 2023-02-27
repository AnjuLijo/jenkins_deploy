pipeline {
    agent any
    stages {
        stage('git checkout') {
            steps {
                git 'https://github.com/anjulijo/jenkins_deploy.git'
            }
        }
        stage('deployment') {
            steps{
                sh 'helm upgrade webapp webapp --recreate-pods'
            }
        }
    }
}
