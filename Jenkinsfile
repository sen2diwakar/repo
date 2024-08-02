pipeline {
    agent any

    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stages {
        stage('Execute Ansible playbook') {
            steps {
                ansiblePlaybook playbook: 'sh_ip_arp.yml', inventory: 'inventory.yaml', disableHostKeyChecking: true
            }
        }
    }
}
