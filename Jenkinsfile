 pipeline{

 agent any
 stages{

 stage('Checkout'){
  steps{
       git branch: 'main', credentialsId: 'git_credentials', url: 'https://github.com/shashikanth-t/jenkins-ansible.git'
       }
 }
 stage('Ansible Execution'){
  steps{  
     ansiblePlaybook credentialsId: 'auser', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml', vaultTmpPath: ''
      }
    }
}
}
