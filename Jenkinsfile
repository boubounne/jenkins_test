pipeline {
    agent any
    stages {
        stage('clone') {
            steps {
                sh "rm -rf *"
                sh "git clone https://github.com/boubounne/jenkins_test"
            }
        }
        stage('build') {
            steps {
                sh "cd jenkins_test/ && javac Main.java"
            }
        }
        stage('run') {
            steps {
                sh "cd jenkins_test/ && java Main"
            }
        }
    }
}
