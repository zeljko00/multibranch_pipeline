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
                    sh 'git config --global credential.helper store'
                    sh "git config --global user.name zeljko00"
          sh "git config --global user.email tripic.zeljko@gmail.com"
      sh "git checkout master"
      sh "git merge -X theirs origin/second-feature"
      sh "git push origin master"
    }
               
            }
        }
    }
}
