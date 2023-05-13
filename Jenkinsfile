pipeline {
    agent any
    stages{
        stage('Print on feature branch'){
            steps {
                sh "echo 'Hello from feature branch!'"
                when {
                    branch "*-feature*"
                }
            }
        }
        stage('Read'){
            steps {
                sh 'cat README.txt'
            }
        } 
    }
}
