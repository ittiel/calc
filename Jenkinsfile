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
        stage ('Code Quality'){
            steps {
                echo 'Todo: sonarcube'
                echo 'Todo: Quality and security plugins (FindBugs, CheckMarx, etc.'
            }
        }
        stage('Release') {
            steps {
                echo 'Releasing'
                sh ' mvn -B release:clean release:prepare release:perform -DdryRun=true'
                //running un dryrun since their are ni credentials set on the jenkins machine, so this will fail
                //sh 'mvn -B release:clean release:prepare release:perform'
            }
        }
        stage('DeplCreate testing env') {
            steps {
                echo 'Todo: Creating env'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Todo: Deploying env'
            }
        }
        stage('Integration/System tests') {
            steps {
                echo 'Todo: Testing'
            }
        }       
    }
}