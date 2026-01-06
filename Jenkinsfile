pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }

    environment {
        COURSE = "Jenkins"
    }

    options {
        timeout(time: 10, unit: 'SECONDS')
        disableconcurrentBuilds()
    }

     Parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    
    stages {
        stage('Build') {
            steps {
                sh '''
                    echo "Build stage"
                    echo "Course is $COURSE"
                    sleep 10
                    env
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                    echo "Test stage"
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    echo "Deploy stage"
                '''
            }
        }
    }

    post {
        always {
            echo 'I will always say Hello again!'
            cleanWs()
        }
        success {
            echo 'I will run if success'
        }
        failure {
            echo 'I will run if failure'
        }
        aborted {
            echo 'Pipeline is aborted'
        }
    }
}
