pipeline{
	agent any
		stages {
			stage('Preperation'){
				steps{ sh 'docker pull centos'
					}
				}
			stage('build'){
				steps{ sh 'docker run -itd -p 85:80 --name testing2_script centos'
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
				}
	}
}
