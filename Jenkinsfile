pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('K8s') {
            steps {
                sh 'kubectl set image deployments/hello-node container-name=c82531/teedytest2024:v1.0'
            }
        }
    }
}
