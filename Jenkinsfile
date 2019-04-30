/* pipeline {
     agent any 
	stages {
		stage ('one') {
			steps {
				echo "Steps Running in stage 1"
			}
		}
		stage ('two') {
			steps {
				input ('Do you want continue..?')
			}
		}
		stage ('three') {
			when {
				not{
					branch "master"
				}
			}
			steps {
				echo "Steps Running in third stage.."
			}
		}
		stage ('four') {
			parallel {
				stage ('Unit Test'){
					steps {
						echo "Running Unit Test stesp in parallel stage of stage 4"
					}
				}
				stage ('Integration Test'){
					
					steps {
						echo "Running the integration test..."
					}
				}
			}
		}
	}	
}*/

pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
