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
stage('Merge'){
             when {
                    branch "second-feature"
                }
            steps {
                script {
                    sh "git config --global user.name zeljko"
          sh "git config --global user.email zeljko@gmail.com"
      sh "git checkout master"
      sh "git merge --strategy=theirs origin/second-feature"
      sh "git push origin master"
    }
               
            }
        }
    }
}
