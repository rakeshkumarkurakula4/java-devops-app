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
        // Maven handles compilation and running
        sh 'mvn compile exec:java -Dexec.mainClass="HelloWorld"'
    }
}
    }
}
