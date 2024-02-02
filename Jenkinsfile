pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo "BRANCH_NAME: ${WEBHOOK_BRANCH}"
                    echo "WEBHOOK_WORKSPACE: ${WEBHOOK_WORKSPACE}"

                    // 根据不同分支执行不同操作
//                     if (env.BRANCH_NAME == 'develop') {
//                         echo "Copying code to API_DEVELOP directory"
//                         sh "cp -r ${WORKSPACE}/* ${WWW_ROOT}/${API_DEVELOP}/"
//                         dir("${env.WWW_ROOT}/${env.API_DEVELOP}") {
//                             // 进入当前目录后，输出当前工作目录
//                             sh "pwd"
//                         }
//                     } else if (env.BRANCH_NAME == 'test') {
//                         echo "Copying code to API_TEST directory"
//                         sh "cp -r ${env.WORKSPACE}/* ${env.WWW_ROOT}/${env.API_TEST}/"
//                         dir("${env.WWW_ROOT}/${env.API_TEST}") {
//                             // 进入当前目录后，输出当前工作目录
//                             sh "pwd"
//                         }
//                     } else {
//                         echo "Branch not recognized, no action taken."
//                     }
                }
            }
        }
    }
    environment {
        WEBHOOK_BRANCH = "${env.BRANCH_NAME}"
        WEBHOOK_WORKSPACE = "${env.WORKSPACE}"
        WWW_ROOT = '/www/wwwroot/jenkins'
        API_TEST = 'test'
        API_DEVELOP = 'develop'
    }
}
