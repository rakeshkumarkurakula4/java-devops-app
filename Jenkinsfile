pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
            }
        }

        stage('Build') {
    steps {
        sh 'mvn clean package'
    }
}

        stage('Run') {
            steps {
                sh 'java HelloWorld'
            }
        }
    }
}
