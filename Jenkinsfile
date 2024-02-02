pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    def changeSets = currentBuild.changeSets
                    def branchName = ''

                    // Assuming Git as SCM, adjust for other SCMs
                    for (changeSet in changeSets) {
                        for (entry in changeSet.items) {
                            branchName = entry.branch
                        }
                    }

                    echo "Triggered by changes in branch: ${branchName}"
                }
            }
        }
    }
}
