pipeline {
    agent any

    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stages {
        stage('Execute Ansible playbook') {
            steps {
                ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'inventory.yaml', playbook: 'sh_ip_arp.yml'
            }
        }
    }
}
