pipeline{
    agent any
    stages{
        stage('Scan & Pull'){
            steps{
                echo "Scan from github..."
                when {
                  changeRequest()
                    steps{
                          echo "Pull project from github..."
                            checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '5f4ed90c-149c-4e56-8d3e-399e6ee2b282', url: 'https://github.com/bestInFridays/HelloWorld']]])
                         }
                }
            }
        }
        post {
          failure {
            echo "Scan & Pull failed."
          }
        }
    }
}