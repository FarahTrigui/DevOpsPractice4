pipeline {
  agent any
  stages {
    stage('Terraform Init') {
      steps { sh 'terraform init' }
    }
    stage('Terraform Plan') {
      steps { sh 'terraform plan' }
    }
    stage('Terraform Apply') {
      steps { sh 'terraform apply -auto-approve' }
    }
    stage('Deploy with Ansible') {
      steps {sh 'ansible-playbook -i inventory.ini playbook.yaml'
  }
}
  }
}
