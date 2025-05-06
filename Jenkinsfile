pipeline {
    agent any

    tools {
        maven 'maven-3.9' // Must match the name you set in Jenkins global tool config
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'eclipse1', url: 'https://github.com/Pal-Cyber/EcliDemo.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}
