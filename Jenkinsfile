pipeline {
    agent any
    environment {
        WWW_ROOT = '/www/wwwroot/jenkins'
        API_TEST = 'test'
        API_DEVELOP = 'develop'
    }
    stages {
        stage('No-op') {
            steps {
                sh 'ls'
            }
        }
        stage('Build') {
            steps {
                script {
                    echo "BRANCH_NAME: ${BRANCH_NAME}"
                    echo "WORKSPACE: ${WORKSPACE}"
                }
            }
        }
    }
    post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
            mail to: 'yinghao@ciandt.com',
                 subject: "Pipeline: ${currentBuild.fullDisplayName}",
                 body: "push ${env.BUILD_URL}"
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
