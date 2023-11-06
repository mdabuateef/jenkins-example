pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage('Build') {
            steps {
                    withMaven {
                        sh 'mvn clean verify sonar:sonar'
                    }
                }
            }
        }
    }
