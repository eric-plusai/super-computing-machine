pipeline {
    agent any
    stages {
        stage('No-ops') {
            steps {
                sh 'ls'
		echo 'Hello Jenkins'
            }
        }
    }
    post {
        success {
            mail to: 'eric.shuai.wang@plus.ai',
                 subject: "Succeeded Pipeline: ${currentBuild.fullDisplayName}",
                 body: "Build url: ${env.BUILD_URL}"
        }
    }
}
