pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '7fc6f676-451f-4e16-b52d-02049fa25487', url: 'https://github.com/GauravBarua/Inventory-Management-System-Spring-Boot.git']]])
                  }
        }
        stage('Build'){
            steps {
                git credentialsId: '7fc6f676-451f-4e16-b52d-02049fa25487', url: 'https://github.com/GauravBarua/Inventory-Management-System-Spring-Boot.git'
                
            }
        }
        stage('Test'){
            steps{
                echo "Success!"
                
            }
        }
    }
}
