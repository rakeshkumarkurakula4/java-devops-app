pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Cloning code...'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t java-app .'
            }
        }

        stage('Docker Run') {
            steps {
                sh '''
                docker stop java-app || true
                docker rm java-app || true
                docker run -d --name java-app java-app
                '''
            }
        }
    }
}
