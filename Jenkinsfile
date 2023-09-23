pipeline {
	agent {
		label {
		 label 'built-in'
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
			   stage ('git clone') {
		    steps { 
			    dir ("/mnt/multibranch1") {
			    }
			  sh "git clone https://github.com/keshavkale123/multibranch-pipeline.git -b 23Q1"
			      }
				}
			stage ('23Q1') {
			 steps {
              sh "cp -r /mnt/multibranch1/multibranch-pipeline/index.html /var/www/html/"
                sh "chmod -R 777 /var/www/html"
			} 
	
		} 
		   }
}
