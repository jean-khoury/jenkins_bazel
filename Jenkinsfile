pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'bazel buildd ...'
            }
        }

    }
}