pipeline {
    agent any
    stages {
         stage('Plan') {
            steps {
                script {
                    currentBuild.displayName = "${version}"
                }
                sh 'terraform init -input=false'
                sh 'terraform workspace select ${environment}'
                sh "terraform plan -input=false -out tfplan -var 'version=${version}' --var-file=environments/${environment}.tfvars"
                sh 'terraform show -no-color tfplan > tfplan.txt'
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
