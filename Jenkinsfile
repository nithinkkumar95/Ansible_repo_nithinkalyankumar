pipeline {
    agent { label 'server1' }
    stages {
        stage('Node_Exporter Installation') {
            steps {
                sh '''
                export ANSIBLE_HOST_KEY_CHECKING=False
                ansible-playbook -i /etc/ansible/hosts /root/prometheus.yml -vvv
                '''
            }
        }
        stage('Prometheus Installation') {
            steps {
                sh '''
                export ANSIBLE_HOST_KEY_CHECKING=False
                ansible-playbook -i /etc/ansible/hosts /root/prometheus.yml -vvv
                '''
            }
        }
    }
}
