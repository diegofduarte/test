pipeline {
    agent none 
    stages {
        stage('Example Build') {
            podTemplate(label: 'mypod') {
                node('mypod') {
                    stage('Run shell') {
                        sh 'echo hello world'
                    }
                }
            }
        stage('Example Test') {
            agent { docker 'openjdk:8-jre' } 
            steps {
                echo 'Hello, JDK'
                sh 'java -version'
            }
        }
    }
}