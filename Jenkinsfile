pipeline {
	agent any
    stages {
        stage('Build on k8 ') {
            steps {      
		    withCredentials([usernamePassword(credentialsId: 'acr-credentials', passwordVariable: 'AZURE_CLIENT_SECRET', usernameVariable: 'AZURE_CLIENT_ID')]){
                        sh 'pwd'
		        sh 'ls -ltr'
                        sh 'pwd'
                        sh 'helm upgrade --install petclinic-app petclinic  --set image.repository=marijavregistry.azurecr.io/cloudfreak1/petclinic, acr-credentials --set image.tag=1'
		    }		
            }           
        }
    }
}
