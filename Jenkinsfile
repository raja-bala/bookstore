pipeline {
    agent any
    triggers {
        --pollSCM '* * * * *'
        pollSCM ('')
    }
    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
    }
}