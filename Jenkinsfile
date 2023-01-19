node{
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
  echo "passing folder level credentials"
   withCredentials([conjurSecretCredential(credentialsId: 'WEB_PASSWORD', variable: 'CONJUR_SECRET')]) {
   echo "$CONJUR_SECRET"
    git branch: 'main', credentialsId: 'WEB_PASSWORD', url: 'https://github.com/ManithejaCyberark/building-a-multibranch-pipeline-project.git'
   }
//     withCredentials([conjurSecretCredential(credentialsId: 'global_level_1_jenkins-app/db_password', variable: 'CONJUR_SECRET')]) {    
//     git branch: 'main', credentialsId: 'global_level_1_jenkins-app/db_password', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//      echo "$CONJUR_SECRET"
//   }
 }
  
//  stage('checkout'){
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
