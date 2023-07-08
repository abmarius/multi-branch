pipeline {
	agent any 
	stages{
		stage('1-clonecode'){
			steps{
			git branch: 'main', credentialsId: 'github-cred', url: 'https://github.com/abmarius/multi-branch.git'
			}
		}
		stage('2-s2'){
			steps{
				sh 'lscpu'
				sh 'whoami'
			}
		}
		stage('3-s3'){
			steps{
				sh 'df -h'
				sh 'touch team6'
			}
		}
		stage('4-s4'){
			steps{
				sh 'pwd'
				sh 'du -h'
			}
		}
        stage('5-s5'){
			parallel {
				stage('p1'){
					steps{
						echo "first parallel-stage"
					}
				}
				stage('p2'){
					steps{
						echo "second parallel-stage"
					}
				}
			}
        }
        stage('6-scriptdemo'){
            steps{
                sh 'bash -x  /var/lib/jenkins/workspace/team6-demo1-pipeline/scriptdemo.sh'
            }
        }
	}
}
