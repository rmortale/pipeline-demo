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
                sh "mvn --batch-mode -V -e test deploy -Dsurefire.useFile=false"
            }
        }
        stage('--package--') {
            steps {
                echo "mvn package"
            }
        }
    }
}
