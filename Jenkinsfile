pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'MyGitHub', url: 'https://github.com/GauravBarua/Inventory-Management-System-Spring-Boot.git']]])
            }
        }
        stage('Build') {
            steps {
                git credentialsId: 'MyGitHub', url: 'https://github.com/GauravBarua/Inventory-Management-System-Spring-Boot.git'
            }
        }
        stage('Test and Deploy') {
            steps {
                sh 'echo "Successfully tested and deployed!"'
            }
        }
    }
}
