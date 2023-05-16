pipeline{
  agent any
   stages{
     stage("manual"){
       steps{
//         echo "NTT Issue"
//       withCredentials([conjurSecretCredential(credentialsId: 'private_key', variable: 'CONJUR_SECRET')]) {
//            sh "echo $CONJUR_SECRET | base64"
//          }
         echo "TJX issue"
         withCredentials([conjurSecretCredential(credentialsId: 'tjx_cred_testing_jenkinsfile', variable: 'CONJUR_SECRET_TJX_ISSUE')]) {
               sh "echo $CONJUR_SECRET_TJX_ISSUE | base64"
            }
       }
     }
   }
}
