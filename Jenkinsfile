pipeline{
  agent {
       node { label 'masternode' } 
    //node {label 'jenkins-slave1'}
//       node {label 'worker-1'}
   }
  
        stages{
         stage("git checkout"){
             steps{
                 echo "cloned the code from git repo"
             }
         }    
      stage("test credentials"){
                steps{
                    withCredentials([conjurSecretCredential(credentialsId: 'db_password', variable: 'CONJUR_SECRET')]) {
                        sh 'echo $CONJUR_SECRET | base64'
                    }
                }
            }
        stage("test manual secret"){
            steps{
                withCredentials([conjurSecretCredential(credentialsId: 'secret_2', variable: 'CONJUR_SECRET')]) {
                  sh 'echo $CONJUR_SECRET | base64'   
                }
            }
        }
    }
}
