pipeline {
	agent any 
	stages{
		stage('1-clonecode'){
			steps{
			checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'githubID', url: 'https://github.com/abmarius/multi-branch.git']])
			}
		}
		stage('2-member-name1'){
			steps{
				echo "member 1: kingsly nr"
			}
		}
		stage('3-member-name2'){
			steps{
				echo "member 2: ifeanye"
			}
		}
		stage('4-member-name3'){
			steps{
				echo "member 3: bruno"
			}
		}
        stage('5-member-name4'){
            steps{
                echo "member 4: eric"
            }
        }
        stage('6-member-name5'){
            steps{
                echo "member 5: bazil"
            }
        }
	}
}