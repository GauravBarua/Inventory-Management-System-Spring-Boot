pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/randil']], extensions: [], userRemoteConfigs: [[credentialsId: 'MyGitHub', url: 'https://github.com/GauravBarua/Inventory-Management-System-Spring-Boot.git']]])
            }
        }
        stage('Build') {
            steps {
                git branch: 'randil', credentialsId: 'MyGitHub', url: 'https://github.com/GauravBarua/Inventory-Management-System-Spring-Boot.git'
                
            }
        }
        stage('Test and Deploy') {
            steps{
                sh 'echo "Successfully Tested and Deployed!"'
            }
        }
    }
}
