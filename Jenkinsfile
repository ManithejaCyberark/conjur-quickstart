node{
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
  echo "passing folder level credentials"
    withCredentials([conjurSecretCredential(credentialsId: 'folder_level_1_jenkins-app/db_password', variable: 'CONJUR_SECRET')]) {    
    git branch: 'main', credentialsId: 'folder_level_1_jenkins-app/db_password', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
  }
 }
  
//  stage('checkout'){
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
