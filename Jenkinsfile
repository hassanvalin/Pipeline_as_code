def name = "Hello"
def props = readProperties file:'branch-specific.properties'

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Hello 6"
                echo "The name is: ${name}"
                echo "The next branch is : ${props.nextBranchName}"
            }
        }
    }
}
