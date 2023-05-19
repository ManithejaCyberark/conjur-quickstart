// pipeline{ //NTT
//   agent any
//    stages{
//      stage("manual"){
//        steps{
// //         echo "NTT Issue"
// //       withCredentials([conjurSecretCredential(credentialsId: 'private_key', variable: 'CONJUR_SECRET')]) {
// //            sh "echo $CONJUR_SECRET | base64"
// //          }
//          echo "TJX issue"
//          withCredentials([conjurSecretCredential(credentialsId: 'tjx_cred_testing_jenkinsfile', variable: 'CONJUR_SECRET_TJX_ISSUE')]) {
//                sh "echo $CONJUR_SECRET_TJX_ISSUE | base64"
//             }
//        }
//      }
//    }
// }

// tjx
pipeline{
  agent any
  stages{
     stage("checking host id"){
       steps{
//           withCredentials([conjurSecretCredential(credentialsId: 'TJX_db_password', variable: 'CONJUR_SECRET_PASSWORD_MANUAL')]) {
//                sh "$CONJUR_SECRET_PASSWORD_MANUAL | base64"
//             }
//             withCredentials([conjurSecretCredential(credentialsId: 'TJX_SECRET_FROM_GITHUB', variable: 'CONJUR_SECRET')]) {
//                 sh "echo $CONJUR_SECRET | base64"
//             }
//          withCredentials([conjurSecretCredential(credentialsId: 'global_password_from_pipeline', variable: 'CONJUR_SECRET')]) {
//                 sh "echo $CONJUR_SECRET | base64"
//             }
        
          withCredentials([conjurSecretCredential(credentialsId: 'global_credentials_jenkins_pipeline_from_github', variable: 'CONJUR_SECRET_FROM_PIPELINE')]) {
                   sh 'echo $CONJUR_SECRET_FROM_PIPELINE | base64'
              }
//           withCredentials([conjurSecretCredential(credentialsId: 'db_password_tjx', variable: 'CONJUR_SECRET')]) {
//                  sh "echo $CONJUR_SECRET | base64"
//               }
       }
     }
  }
}
