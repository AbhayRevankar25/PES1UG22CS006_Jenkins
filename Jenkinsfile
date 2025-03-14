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
                    sh './NON_EXISTENT_FILE '  // Run the compiled binary
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
            script {
                echo 'Pipeline failed'
            }
        }
    }
}
