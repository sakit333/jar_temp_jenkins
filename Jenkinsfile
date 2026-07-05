pipeline {
    agent any

    tools {
        maven 'maven'
    }
    stages {
        stage("Build stage") {
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo "maven success"
                }
                failure {
                    echo "maven failure"
                }
            }
        }    
    }
    post {
        success {
            echo "build success"
        }
        failure {
            echo "build failure"
        }
    }
}