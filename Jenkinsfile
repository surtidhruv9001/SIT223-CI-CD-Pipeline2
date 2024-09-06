pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'echo Build step here'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'echo Test step here'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'echo Deploy step here'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'Build was successful!'
            mail to: 'surtidhruv9001aus@gmail.com',
                  subject: "Build Successful",
                  body: "The build was successful."
        }
        failure {
            echo 'Build failed!'
            mail to: 'surtidhruv9001aus@gmail.com',
                  subject: "Build Failed",
                  body: "The build failed. Please check the Jenkins logs."
        }
    }
}

