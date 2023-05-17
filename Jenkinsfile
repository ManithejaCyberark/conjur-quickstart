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
          withCredentials([conjurSecretUsername(credentialsId: 'global_from_pipeline_github', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
              sh "echo $CONJUR_SECRET"
//               git branch: 'main', credentialsId: 'global_from_pipeline_github', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
          }
       }
     }
  }
}
