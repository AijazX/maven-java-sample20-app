pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               bat "rmdir  /s /q maven-java-sample20-app"
                bat "git clone https://github.com/AijazX/maven-java-sample20-app.git"
                bat "mvn clean -f maven-java-sample20-app"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f maven-java-sample20-app"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f maven-java-sample20-app"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f maven-java-sample20-app"
            }
        }
    }
}
