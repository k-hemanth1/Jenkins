pipeline {
    agent {
        node{
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = "Jenkins"
    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh"""
                       echo 'Build stage'
                       echo $COURSE
                    """
                }
            }
        }
       
        stage('Test') {
            steps {
                script{
                    sh"""
                       echo 'Build stage'
                    """
                }
            }
        }

        stage('Deploy') {
            steps {
             script{
                 sh"""
                     echo 'Build stage'
                    """
                }
            }
        }
    }
    post{
        always{
            echo ' I Will always say Hello again!'
             cleanWs()
        }
        success{
            echo 'I will run if success'
        }
        failure{
            echo 'I will run if success'
        }
    }
}