pipeline {
    agent any
    stages {
        stage("Compile") {
            steps {
                // gradlew 파일에 실행 권한을 추가하는 명령어
                sh 'chmod +x ./gradlew'
                sh './gradlew compileJava'
            }
        }
        stage("Build") {
            steps {
                sh './gradlew build'
            }
        }
        stage("Unittest") {
            steps {
                sh './gradlew test'
                echo 'hi'
            }
        }
    }
}