node{
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
  echo "passing folder level credentials"
   withCredentials([conjurSecretUsername(credentialsId: 'password1', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
    echo "secret value of is: $CONJUR_SECRET and $USERNAME"
    //git branch: 'main', credentialsId: 'ManithejaCyberark', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
    echo "completed"
   }
  echo "completed"
 }
 
//  stage('checkout'){
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
