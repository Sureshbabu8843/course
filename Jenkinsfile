pipeline{
	agent any
		stages {
			stage('Preperation'){
				steps{ echo 'this is preperation stage'
					}
				}
			stage('build'){
				steps{ echo 'this is build stage'
					}
				}
			stage('test'){ 
				steps{ echo 'this is testing stage'
					}
				}
			stage('deploy'){
				steps{ input ('Do you want to proceed?')
						echo 'this is deploy stage'
					}
				
			post {
				success {
					mail to: 'gsureshbabu4321@gmail.com', subject: 'job is success', body: 'this is test'
						}
				}
			}
	}
}
