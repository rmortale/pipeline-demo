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
               
            withMaven(
                // Maven installation declared in the Jenkins "Global Tool Configuration"
                maven: 'm339')
                sh "mvn --batch-mode -V -e test deploy -Dsurefire.useFile=false"
            } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe & FindBugs reports...
        }

        stage('--package--') {
            steps {
                echo "mvn package"
            }
        }
    }
}
