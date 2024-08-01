pipeline {
    agent any

    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stage('Run Ansible Playbook') {
          steps {
              // Run the Ansible playbook
              sh '''
              ansible-playbook -i inventory sh_ip_arp.yml
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
