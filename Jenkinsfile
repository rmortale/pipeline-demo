pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                echo "mvn clean"
            }
        }
        stage('--test--') {
            steps {
                echo "mvn test"
            }
        }
        stage('--package--') {
            steps {
                echo "mvn package"
            }
        }
    }
}
