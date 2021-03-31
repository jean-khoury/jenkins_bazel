pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'bazel build ...'
                publishChecks name: 'BuildCheck', title: 'Build Check', summary: 'Calling Bazel build on the repo'
            }
        }
            stage('Test') {
            steps {
                script{
                    sh 'echo ehfweu'
                    publishChecks name: 'TestCheck', title: 'Test Check', summary: 'Calling Bazel test on the repo'
                }
            }
        }

            stage('Deploy') {
            steps {
                script{
                    sh 'echo deploying'
                // try{
                // sh 'echo deploying'

                // publishChecks name : 'DeployCheck' , title: 'Deployment Check', summary :'Deploying the build artifacts' 
                // }
                // catch (exp){
                //     publishChecks name : 'Deploy Check Failure' , title: 'Deployment Check Failure', summary :'Deploying the build artifacts', conclusion : 'FAILURE' , text : exp.message
                // }
                }
            }
            
        }
    }
}
