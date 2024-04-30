pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "$MAVEN_HOME"
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
