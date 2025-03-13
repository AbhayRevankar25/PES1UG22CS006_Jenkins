pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output PES1UG22CS006-1.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'  // Run the compiled binary
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application is done...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
