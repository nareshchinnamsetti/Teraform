pipeline {
    agent any
    stages {
        stage('Copy') {
      
            steps {
                echo 'Copy Repo'
                sh 'sudo cp /var/lib/jenkins/workspace/Terraform-Pipeline-Job ./jenkins/'
                
            }
        }
       
       stage('Initialize Terraform') {
      
            steps {
                echo 'Parsing Terraform command'
                sh 'sudo /var/lib/jenkins/workspace/Terraform-pipelin-Job terraform init ./jenkins/'
                
            }
        }
        stage('Terraform Plan') {
      
            steps {
                echo 'Terrafrom Plan Command'
                sh 'terraform plan'
                
            }
        }
        stage('Terraform Apply') {
           
            steps {
                echo 'Terraform Apply command'
                sh 'terraform apply'
            }
        }
    }
}
