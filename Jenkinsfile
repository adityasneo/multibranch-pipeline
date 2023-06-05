pipeline{
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Hello World Aditya"
            }
        }
        stage("fix branch") {
          when {
            branch "fix-*"
          }
          steps {
            sh '''
              cat README.md
            '''
          }
         }
         stage("Test") {
            steps {
                echo "Test Aditya"
            }
        }
         stage("PR branch") {
          when {
            branch "PR-*"
          }
          steps {
            echo 'Runs only for PRs'        
           }
          }
    }
}
