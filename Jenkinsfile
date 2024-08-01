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
                script {
                    ansiblePlaybook(
                        playbook: '/home/netbotadmin/sh_ip_arp.yml',
                        inventory: '/home/netbotadmin/inventory',
                        colorized: true)
                    // Ensure Ansible is in the PATH
                    sh 'export PATH=$PATH:/usr/bin/ansible'

                    // Run the playbook
                    sh 'ansible-playbook -i inventory playbook'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
