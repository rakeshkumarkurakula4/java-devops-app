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
                sh 'mvn clean compile'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Run') {
    steps {
        sh 'java -cp target/java-app-1.0.jar HelloWorld'
    }
}
    }
}
