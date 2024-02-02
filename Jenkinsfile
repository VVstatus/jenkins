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
  environment {
    WWW_ROOT = '/www/wwwroot'
    API_TEST = 'api.ddmj-test.ananew.cn'
    API_DEVELOP = 'api.ddmj-dev.ananew.c'
  }
}