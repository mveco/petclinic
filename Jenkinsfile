pipeline {
	agent any
    stages {
        stage('Build on k8 ') {
            steps {           
                        sh 'pwd'
		        sh 'ls -ltr'
                        sh 'pwd'
                        sh 'helm upgrade --install petclinic-app petclinic  --set image.repository=marijavregistry.azurecr.io/cloudfreak1/petclinic --set image.tag=1'
              			
            }           
        }
    }
}
