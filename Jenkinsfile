pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage('Build') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    withMaven {
                        sh 'mvn clean verify sonar:sonar'
                    }
                }
            }
        }
    }
}

