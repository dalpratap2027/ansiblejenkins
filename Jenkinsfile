pipeline {
  agent { label ${LABEL_NAME} }

  stages {
    stage('code') {
      steps {
        git url: "", branch: "main"
      }
    }
     stage('ANSIBLE PLAYBOOK') {
      steps {
        ansiblePlaybook(
          playbook: 'ansible/deploy.yml'
          inventory: 'ansible/hosts.ini'
        )
      }
    }
    
  }
}
