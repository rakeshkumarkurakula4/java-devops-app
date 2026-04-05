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
                sh 'sudo docker build -t java-app .'
            }
        }

        stage('Docker Run') {
            steps {
                sh '''
                sudo docker stop java-app || true
                sudo docker rm java-app || true
                sudo docker run -d --name java-app java-app
                '''
            }
        }
    }
}
