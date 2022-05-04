pipeline{
    agent any
    tools {
      terraform 'Terraform-12'
    }
    stages{        
		stage('Git Checkout'){
            steps{
                git branch: 'main', credentialsId: '92f02f32-e773-4b23-a361-869b26b88c3a', url: 'https://github.com/kandisridhar/terraform-jenkins-declarative.git'
            }
		}
        stage('Terraform Init'){
            steps{
                sh label: '', script: 'terraform init'
            }    
        }
        stage('Terraform Apply'){
            steps{
                sh label: '', script: 'terraform apply -auto-approve'
            }    
        }
    }
}
