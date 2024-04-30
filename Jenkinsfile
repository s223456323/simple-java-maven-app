pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "$JAVA_HOME"
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
