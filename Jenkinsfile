pipeline {
    agent {
        node{
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = "Jenkins"
    }
     options {
        timeout(time: 10, unit: 'SECONDS') 
    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh"""
                       echo 'Build stage'
                       echo $
                       sleep 10
                       env
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
        aborted {
            echo 'pipeline is aborted'
        }
    }
}