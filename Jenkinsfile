pipeline {
    agent any

    stages {
        stage('Example') {
            steps {
                dir('path/to/directory') {
                    // Commands or steps to be executed in the specified directory
                    sh 'echo "Hello, Jenkins!"'
                    sh 'ls -al'
                }
            }
        }
    }
}
