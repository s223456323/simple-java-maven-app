pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "$M2_HOME"
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
