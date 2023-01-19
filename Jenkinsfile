node{
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
  echo "passing folder level credentials"
   withCredentials([conjurSecretUsername(credentialsId: 'error_1', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')])  {
   echo "$CONJUR_SECRET"
    git branch: 'main', credentialsId: 'error_1', url: 'https://github.com/ManithejaCyberark/building-a-multibranch-pipeline-project.git'
    
   }
 }
//  stage('checkout'){
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
