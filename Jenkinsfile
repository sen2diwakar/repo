pipeline {
    agent any

    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stages {
        stage('Run Ansible Playbook') {
            steps {
                // Run the Ansible playbook
                sh '''
                pwd
                '''
                sh '''
                chdir /home/netbotadmin
                '''
                sh '''
                ansible-playbook -i inventory sh_ip_arp.yml
                '''
            }
        }
    }
}
