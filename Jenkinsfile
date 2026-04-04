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
        sh 'mvn exec:java -Dexec.mainClass="HelloWorld"'
    }
}
    }
}
