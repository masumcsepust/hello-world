pipeline {
    agent any  

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/masumcsepust/hello-world'
            }
        }

        stage('Build Application') {
            steps {
                script {
                    sh 'dotnet build --configuration Release'
                }
            }
        }
    }

    post {
        success {
            echo "Build completed successfully!"
        }
        failure {
            echo "Build failed!"
        }
    }
}
