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
                sh 'kubectl set image deployments/hello-node teedytest2024=c82531/teedytest2024:v1.0'
            }
        }
    }
}
