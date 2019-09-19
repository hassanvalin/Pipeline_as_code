def name = "Hello"

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               script {
                   
                  // Reading property file and defining variables. To achieve this we need to install 'Pipeline Utility Steps’ plugin
                  def properties = readProperties file: 'branch-specific.properties'
                  env.GIT_REPO =  properties.GitURL
                   
                   
                  echo "Running build ${JOB_NAME} # ${BUILD_NUMBER} on git repo ${env.GIT_REPO} branch ${properties.nextBranchName}"
               }
            }
        }
        stage('Test') {
            steps {
                echo "The Git repo is : ${env.GIT_REPO}"
            }
        }    
    }
}
