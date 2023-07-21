pipeline{
    agent any
    stages{
        // stage("print hello"){
        //     steps{
        //         echo "Hello jenkins"
        //     }
        // }
        stage("Dev team credentials"){
            steps{
                echo "Dev team credentials"
                withCredentials([conjurSecretCredential(credentialsId: 'f259e29b-51a8-4cce-a9ae-de60d08fd11b', variable: 'CONJUR_SECRET_DEV_TEAM_1')]) {
                   sh 'echo $CONJUR_SECRET_DEV_TEAM_1 | base64'
                }
             }
        }
        stage("test pipeline cred"){
            steps{
                echo "test-pipeline cred"
                 withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET_TEST_PIPELINE')]) {
                  sh 'echo $CONJUR_SECRET_TEST_PIPELINE | base64'
                }
            }
        }
    }
}


// pipeline{ 
//   //NTT
//   agent any
//    stages{
//      stage("manual"){
//        steps{
//         echo "NTT Issue"
//       withCredentials([conjurSecretCredential(credentialsId: 'private_key', variable: 'CONJUR_SECRET')]) {
//            sh "echo $CONJUR_SECRET | base64"
//          }
// //          echo "TJX issue"
// //          withCredentials([conjurSecretCredential(credentialsId: 'tjx_cred_testing_jenkinsfile', variable: 'CONJUR_SECRET_TJX_ISSUE')]) {
// //                sh "echo $CONJUR_SECRET_TJX_ISSUE | base64"
// //             }
//        }
//      }
//    }
// }

// // tjx
// pipeline{
//   agent any
//   stages{
//      stage("checking host id"){
//        steps{
// //           withCredentials([conjurSecretCredential(credentialsId: 'TJX_db_password', variable: 'CONJUR_SECRET_PASSWORD_MANUAL')]) {
// //                sh "$CONJUR_SECRET_PASSWORD_MANUAL | base64"
// //             }
// //             withCredentials([conjurSecretCredential(credentialsId: 'TJX_SECRET_FROM_GITHUB', variable: 'CONJUR_SECRET')]) {
// //                 sh "echo $CONJUR_SECRET | base64"
// //             }
// //          withCredentials([conjurSecretCredential(credentialsId: 'global_password_from_pipeline', variable: 'CONJUR_SECRET')]) {
// //                 sh "echo $CONJUR_SECRET | base64"
// //             }
//          try{
//           withCredentials([conjurSecretCredential(credentialsId: 'global_credentials_jenkins_pipeline_from_github', variable: 'CONJUR_SECRET_FROM_PIPELINE')]) {
//                    sh 'echo $CONJUR_SECRET_FROM_PIPELINE | base64'
//               }
//          }
//          catch(exc){
//            echo "404 not found"
//            throw
//          }
// //           withCredentials([conjurSecretCredential(credentialsId: 'without-host-configuration', variable: 'CONJUR_SECRET')]) {
// //                        sh "echo $CONJUR_SECRET | base64"
// //                     }
           
         
//          //jenkins -os
// //          withCredentials([conjurSecretCredential(credentialsId: 'global_credentials_jenkins_pipeline_from_github', variable: 'CONJUR_SECRET')]) {
// //                          sh "echo $CONJUR_SECRET | base64"
// //                       }
//        }
//      }
//   }
// }
