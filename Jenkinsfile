pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "build new project"
            }
        }
    }

    post {
        success {
            emailext subject: 'Pipeline Success',
                      body: 'Your pipeline has succeeded.',
                      to: 'y.b.n.udara@email.com'
        }
    }
}
