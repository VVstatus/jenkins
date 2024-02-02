pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo "BRANCH_NAME: ${BRANCH_NAME}"
                    echo "WORKSPACE: ${WORKSPACE}"

                    // 根据不同分支执行不同操作
                    if (BRANCH_NAME == 'develop') {
                        echo "Copying code to API_DEVELOP directory"
                        // sh "cp -r ${WORKSPACE}/* ${WWW_ROOT}/${API_DEVELOP}/"
                        dir("${WWW_ROOT}/${API_DEVELOP}") {
                            // 进入当前目录后，输出当前工作目录
                        }
                    } else if (BRANCH_NAME == 'test') {
                        echo "Copying code to API_TEST directory"
                        // sh "cp -r ${WORKSPACE}/* ${WWW_ROOT}/${API_TEST}/"
                        dir("${WWW_ROOT}/${API_TEST}") {

                        }
                    } else {
                        echo "Branch not recognized, no action taken."
                    }
                }
            }
        }
    }
    environment {
        WWW_ROOT = '/www/wwwroot/jenkins'
        API_TEST = 'test'
        API_DEVELOP = 'develop'
    }
}
