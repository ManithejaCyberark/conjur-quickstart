pipeline{
  
   agent any
  
//   agent {
//        node { label 'executor-v1' } 
//        //node {label 'jenkins-slave1'}
//        // node {label 'worker-1'}
//    }
  
        stages{
         stage("git checkout"){
             steps{
                 echo "cloned the code from git repo"
             }
         }    
          
         stage("test credentials"){
                steps{
                    withCredentials([conjurSecretCredential(credentialsId: 'from_jenkinsfile_github', variable: 'CONJUR_SECRET')]) {
                        sh 'echo $CONJUR_SECRET | base64'
                    }
                }
            }
//         stage("test manual secret"){
//             steps{
//                 withCredentials([conjurSecretCredential(credentialsId: 'password_1_manual', variable: 'CONJUR_SECRET')])  {
//                   //password_1_manual 
//                   sh 'echo $CONJUR_SECRET | base64 '
//                   sh 'echo $CONJUR_SECRET | base64 | base64'
//                 }
//             }
//         }
    }
}
