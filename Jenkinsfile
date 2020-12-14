pipeline{
     agent any
     stages{
          stage('SCM Checkout'){
               steps{
                    git 'https://github.com/isims51461/apache-release-03-cd'
               }
          }
          stage('Execute Ansible Playbook'){
              steps{
                  'ansiblePlaybook credentialsId: 'ansible_user_2', disableHostKeyChecking: true, installation: 'ansible', inventory: 'hosts', playbook: 'release-03.yml'
         }
       }
     }
}

