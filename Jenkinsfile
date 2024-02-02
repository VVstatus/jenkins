pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "JOB_NAME ${env.JOB_NAME}"
                echo "NODE_NAME ${env.NODE_NAME}"
                echo "WORKSPACE ${env.WORKSPACE}"
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}