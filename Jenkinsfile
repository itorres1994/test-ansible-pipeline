pipeline {
  agent any
  stages {
    stage('Checkout SCM') {
      steps {
        git 'https://github.com/itorres1994/test-ansible-pipeline.git' 
      }
    }
    stage('Execute Ansible') {
      steps {
        ansiblePlaybook credentialsId: 'ansible-ssh', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'dev.inv', playbook: 'apache.yml'
      }
    }
  }
}
