pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo "Building the code using Maven"
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo "Running unit tests junit"
                
                echo "Running integration tests junit"
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo "Running code analysis with sonarQube"
            }
        }
        
        stage('Security Scan') {
            steps {
                echo "Performing security scan with sonarQube"
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo "Deploying to staging server with AWS EC2"
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo "Running integration tests on staging environment with Junit"
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo "Deploying to production server with AWS EC2"
            }
        }
    }
    
    post {
        success {
            emailext subject: 'Pipeline Success',
                      body: 'Your pipeline has succeeded.',
                      to: 'y.b.n.@email.com',
                      attachLog: true
        }
        failure {
            emailext subject: 'Pipeline Failure',
                      body: 'Your pipeline has failed.',
                      to: 'y.b.n.@email.com',
                      attachLog: true
        }
    }
}
