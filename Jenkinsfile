pipeline {
    agent any
    stages {
        stage('Set Terraform path') {
 steps {
 script {
 def tfHome = tool name: 'terraform'
 env.PATH = "${tfHome}:${env.PATH}"
 }
 sh 'terraform --version'
 
 }
 }
        stage ('Version'){
            steps{
                echo 'terraform'
                sh 'terraform --version -input=false'
                
            }
        }

        stage('Terraform destroy') {
           
            steps {
                echo 'Terraform destroy command'
                sh 'terraform destroy -auto-approve'
            }
        }
    }
}
