pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    tools {
        maven 'Maven'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests -Dskip.unit.tests=true'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
