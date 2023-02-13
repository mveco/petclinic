pipeline {
	agent any
    stages {
        stage('Build on k8 ') {
            steps {           
                        sh 'pwd'
		        sh 'ls -ltr'
                        sh 'pwd'
                        sh 'C:/Program Files/helm-v3.11.0-windows-amd64/windows-amd64/helm upgrade --install petclinic-app */helm/petclinic  --set image.repository=marijavregistry.azurecr.io/cloudfreak1/petclinic'
              			
            }           
        }
    }
}
