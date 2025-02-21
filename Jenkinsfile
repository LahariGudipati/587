pipeline {
    agent any  
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/LahariGudipati/587.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'  
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test' 
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application'  
            }
        }
    }
    
    post {
        success {
            echo 'Build and tests were successful!'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}
