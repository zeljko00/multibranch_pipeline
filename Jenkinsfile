pipeline {
    agent any
    stages{
        stage('Print on feature branch'){
             when {
                    branch "*-feature*"
                }
            steps {
                sh "echo 'Hello from feature branch!'"
               
            }
        }
        stage('Read'){
            steps {
                sh 'cat README.txt'
            }
        } 
    }
}
