def name = "Hello"
def props = readProperties file:'branch-specific.properties'

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "The next branch is : ${props.nextBranchName}"
               // script {
                   // def properties = readProperties file: 'branch-specific.properties'
                   // echo "Running build ${JOB_NAME} # ${BUILD_NUMBER} on git repo ${properties.GitURL} branch ${properties.nextBranchName}"
               // }
            }
        }
    }
}
