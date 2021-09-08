pipeline {
    agent none
    stages {
        stage('Terraform Apply ap-southeast-1') {
		    agent {
               label 'agent1'
            }
            environment {
                AWS_DEFAULT_REGION="ap-southeast-2"
            }
            steps {
			    echo "****ap-southeast-1***"
				
     sh '''
                  pwd
		  whoami
                  ls -lrt
                 

                  '''
	sh "terraform version"	
          sh "terraform init" 
 sh "terraform plan"

              
            }
        }
    }
	}



