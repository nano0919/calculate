pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Compile') {
            steps {
                script {
                    // 권한 부여
                    sh 'chmod +x gradlew'
                    // Gradle 실행
                    sh './gradlew compileJava'
                }
            }
        }
        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }
        stage('Unit Test') {
            steps {
                sh './gradlew test'
            }
        }
    }
}
