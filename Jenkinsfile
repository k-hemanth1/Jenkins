pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build stage'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage'
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