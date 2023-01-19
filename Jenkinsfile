node{
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
  echo "passing folder level credentials"
   withCredentials([conjurSecretCredential(credentialsId: 'jenkins-app/db_password', variable: 'CONJUR_SECRET')]) {
   echo "$CONJUR_SECRET"
    git branch: 'main', credentialsId: 'jenkins-app/db_password', url: 'https://github.com/ManithejaCyberark/building-a-multibranch-pipeline-project.git'
    
   }
 }
//  stage('checkout'){
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
