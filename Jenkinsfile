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
				  sh "aws s3 ls"
                                 sh "aws s3 cp  --recursive . s3://cloudyeticicd1/TERRAFORMSCRIPT_EKS" 
          sh "terraform init" 
 sh "terraform plan"

              
            }
        }
    }
	}



