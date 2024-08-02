pipeline {
    agent any

    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stages {
        stage('Execute Ansible playbook') {
            steps {
        sh 'ansible-galaxy collection install -r requirement.yml'
        sh 'ansible-playbook -i inventory.yaml sh_ip_arp.yml'
      }
        }
    }
}
