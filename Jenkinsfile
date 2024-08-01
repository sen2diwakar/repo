pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                ansible-playbook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'inventory', playbook: 'sh_ip_arp.yml'  
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
