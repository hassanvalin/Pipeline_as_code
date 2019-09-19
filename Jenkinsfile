def name = "Hello"

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               script {
                  def properties = readProperties file: 'branch-specific.properties'
                  echo "Running build ${JOB_NAME} # ${BUILD_NUMBER} on git repo ${properties.GitURL} branch ${properties.nextBranchName}"
                   echo "The other parameters are : ${properties.git.hello_deploy.github_ssh_url}" 
               }
            }
        }
    }
}
