pipeline{
    agent any
    stages{
        stage('Scan'){
            steps{
                echo "Scan from github..."
                timeout(time: 3, unit: 'SECONDS'){

                }
            }
        }
        stage('Pull'){
            steps{
                echo "Pull project from github..."
                if(currentBuild.changeSets.size()>0){
                    checkout('https://github.com/bestInFridays/HelloWorld.git')
                }else{
                 echo "No changes, nothing to pull"
                }
            }
        }
    }
}