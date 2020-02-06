pipeline {
    agent any
    
    tools {
        maven 'M3'
    }
    
    stages {
        stage('checkout'){
            steps {
                sh 'echo "Checkout stage"'
                git url:'https://github.com/Boucrou/simple-boot.git'
            }
        }
        stage('compile'){
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('test'){
            steps {
                sh 'mvn test'
            }
        }
        stage('package'){
            steps {
                sh 'mvn package'
            }
        }
    }
}