pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/ittiel/calc.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling'
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Unit testing'
                sh 'mvn test'
            }
        }
        stage ('Codee Quality'){
            steps {
                echo 'sonarcube'
                echo 'findbug'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}