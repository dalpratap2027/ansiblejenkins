pipeline {
  agent { label ${LABEL_NAME} }

  stages {
    stage('code') {
      steps {
        git url:"https://github.com/dalpratap2027/ansiblejenkins.git", branch: "main"
      }
    }
     stage('ANSIBLE PLAYBOOK') {
      steps {
        ansiblePlaybook(
          playbook: 'ansible/deploy.yml'
          inventory: 'ansible/hosts.ini'
          credentialsId:'${SSH_KEY}'
        )
      }
    }
    
  }
}
