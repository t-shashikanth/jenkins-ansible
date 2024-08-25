 pipeline{

 agent any

 stages{

 stage('Checkout'){
  steps{
       git branch: 'main', credentialsId: 'gitCredentials', url: 'https://github.com/shashikanth-t/jenkins-ansible.git'
       }
 }
 stage('AnsibleExecution'){
  steps{
     ansiblePlaybook credentialsId: 'auser', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml', vaultTmpPath: ''  
      }
    }
}
 }
