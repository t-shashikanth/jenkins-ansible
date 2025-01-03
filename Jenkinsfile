 pipeline{

 agent any

 stages{

 stage('Chec kout'){
  steps{
  git branch: 'main', credentialsId: 'git_Credentials', url: 'https://github.com/t-shashikanth/jenkins-ansible.git'
       }
 }
 stage('Ansible Execution'){
  steps{

 ansiblePlaybook credentialsId: 'auser', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml', vaultTmpPath: ''
 
      }
    }
}
 }
