pipeline {
    agent any

    stages {

        
        stage('Get Dependencies') {
            steps {
                bat 'flutter pub get'
            }
        }


        stage('Test') {
            steps {
                bat 'flutter test'
            }
        }

        stage('Build') {
            steps {
                bat 'flutter build web'
            }
        }
    }

    post {
        success {
            echo 'Flutter build completed successfully!'
        }

        failure {
            echo 'Flutter build failed!'
        }
    }
}