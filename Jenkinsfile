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
