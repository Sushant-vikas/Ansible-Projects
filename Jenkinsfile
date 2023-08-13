
pipeline {
    agent any 
    stages {
        stage('Preparing') {
            steps{
                sh 'echo Preparing'
            }
        }
        stage('Git Pulling') {
            steps{
                git branch: 'main', url: 'https://github.com/Sushant-vikas/Ansible-Projects.git'
            }
        }
        stage('Playbook Initializing') {
            steps{
                sh 'echo Playbook Initializing'
            }
        }
        stage('Playbook Running') {
            
            steps {
                script {
                    ansiblePlaybook credentialsId: 'Ansible-private-key', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'Ansible_project1/hosts.inv', playbook: 'Ansible_project1/appche.yml'
                }
            }
        }
        stage('Playbook deployed') {
            steps{
                sh 'echo Deployment done!!!!'
            }
        }
    }
}
