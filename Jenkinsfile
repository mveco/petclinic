pipeline {
  agent any
    stages {      
       stage('Build on k8 ') {
            steps { 
                    sh 'pwd'      
            }
        }
        stage('Build docker image') {
           steps {
               script {         
                 def customImage = docker.build('petclinic/helm/petclinic', "./docker")
                 docker.withRegistry('https://marijavregistry.azurecr.io', 'acr-credentials') {
                 customImage.push("${env.BUILD_NUMBER}")
                 }                     
           }
        }
	  }
    }
}
