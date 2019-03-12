pipeline {
    agent any
    stages {
        stage ('Version'){
            steps{
                echo 'terraform'
                sh 'terraform --version'
                
            }
        }
       stage('Initialize Terraform') {
      
            steps {
                echo 'Parsing Terraform command'
                sh 'terraform init'
                
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
