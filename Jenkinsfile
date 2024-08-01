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
                    // Ensure Ansible is in the PATH
                    sh 'export PATH=$PATH:/usr/bin/ansible'

                    // Run the playbook
                    sh 'ansible-playbook -i /home/netbotadmin/inventory sh_ip_arp.yml'
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
