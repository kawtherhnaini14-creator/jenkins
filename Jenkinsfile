pipeline {
    agent any

    stages {
        stage('Force Success') {
            steps {
                echo "This build will always succeed!"
            }
        }
    }

    post {
        always {
            echo "Marking build as SUCCESS."
            script {
                currentBuild.result = 'SUCCESS'
            }
        }
    }
}
