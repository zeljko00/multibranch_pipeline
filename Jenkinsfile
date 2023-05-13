pipeline {
    agent any
    stages{
        stage('Clone repo'){
            steps {
                checkout scm
            }
        } 
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
stage('Merge'){
             when {
                    branch "second-feature"
                }
            steps {
                script {
      sh "git checkout master"
      sh "git merge second-branch"
      sh "git push origin master"
    }
               
            }
        }
    }
}
