pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Kaniamuthu/jenkins.git'
            }
        }

        stage('Deploy using Ansible') {
            steps {
                sh '''
                ansible --version
                ansible-playbook -i inventory/hosts playbook.yml
                '''
            }
        }
    }
}
