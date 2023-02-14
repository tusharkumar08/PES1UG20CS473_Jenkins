pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ ./main/hello.cpp -o PES1UG20CS473'
                build job: 'PES1UG20CS473-1'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing Stage"'
                sh './PES1UG20CS473'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deployment stage"'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed during building and testing pipeline'
        }
    }
}
