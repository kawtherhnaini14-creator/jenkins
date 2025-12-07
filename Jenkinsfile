pipeline {
    agent any

    tools {
        // This name must be the same as in Manage Jenkins -> Tools -> Maven installations
        maven 'M2_HOME'
    }

    stages {

        stage('GIT') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/kawtherhnaini14-creator/jenkins.git'
                // if your repo is private, add:
                //    credentialsId: 'jenkins-example-github-pat'
            }
        }

        stage('MAVEN VERSION') {
            steps {
                sh "mvn -version"
            }
        }

        stage('BUILD') {
            steps {
                sh "mvn clean package"
            }
        }
    }
}
