pipeline {
	agent {
		label {
		 label 'master'
		  customWorkspace "/mnt/multibranch"
		  }
		 }
		
		   stages {
		stage ('clean Workspace') {
			steps {
				cleanWs()
			}
		}
		   stage ('git clone') {
		    steps {
			  sh "git clone https://github.com/keshavkale123/multibranch-pipeline.git"
			      }
				}
			stage ('main') {
			 steps {
              sh "cp -r /mnt/multibranch/multibranch-pipeline/index.html /var/www/html/"
                sh "chmod -R 777 /var/www/html"
                  }
			}
			}
		}
