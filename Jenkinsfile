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
                ansible-playbook -i /home/netbotadmin/inventory /home/netbotadmin/sh_ip_arp.yml
                '''
            }
        }
    }

    post {
        always {
            // Archive the results
            archiveArtifacts artifacts: '**/results/*', allowEmptyArchive: true
        }
    }
}
