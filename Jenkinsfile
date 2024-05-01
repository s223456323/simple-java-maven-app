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
            post {
                success {
                    echo "Tests passed, proceeding to next stages"
                    mail subject: 'Tests Passed',
                         body: 'The unit and integration tests passed.',
                         to: 'y.b.n.udara@gmail.com',
                         attachLog: true
                }
                failure {
                    echo "Tests failed, stopping the pipeline"
                    currentBuild.result = 'FAILURE'
                    mail subject: 'Tests Failed',
                         body: 'The unit and integration tests failed.',
                         to: 'y.b.n.udara@gmail.com',
                         attachLog: true
                }
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
            post {
                success {
                    echo "Security scan passed, proceeding to next stages"
                    mail subject: 'Security scan Passed',
                         body: 'Security scan passed.',
                         to: 'y.b.n.udara@gmail.com',
                         attachLog: true
                }
                failure {
                    echo "Security scan failed, stopping the pipeline"
                    currentBuild.result = 'FAILURE'
                    mail subject: 'Tests Failed',
                         body: 'Security scan failed.',
                         to: 'y.b.n.udara@gmail.com',
                         attachLog: true
                }
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
}
