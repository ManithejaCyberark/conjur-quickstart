// agent {
//     node {
//         label 'my-defined-label'
//         customWorkspace '/some/other/path'
//     }
// }
node{
 { 
  label 'master-Node'
 } 
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
  echo "passing folder level credentials"
   withCredentials([conjurSecretUsername(credentialsId: 'from_jenins_file_user1_password', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
    echo "secret value of is: $CONJUR_SECRET and $USERNAME"
    //git branch: 'main', credentialsId: 'ManithejaCyberark', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
    echo "completed"
   }
  echo "completed"
 }
 
//  stage('checkout'){ password3_with_host2 
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
