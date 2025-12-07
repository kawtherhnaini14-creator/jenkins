pipeline {
    agent any

    tools {
        maven 'M2_HOME'
    }

    stages {

        stage('MAVEN VERSION') {
            steps {
                sh "mvn -version"
                // si agent Windows : bat "mvn -version"
            }
        }

        stage('BUILD') {
            steps {
                sh "mvn clean package"
                // si agent Windows : bat "mvn clean package"
            }
        }
    }
}
