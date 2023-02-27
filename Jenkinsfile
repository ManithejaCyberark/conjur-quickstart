node{
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
  echo "passing folder level credentials"
   withCredentials([conjurSecretUsername(credentialsId: 'from_jenkinsfile', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')])   {
    echo "password2 and configured with host2"
    echo "secret value of is: $CONJUR_SECRET and $USERNAME"
  git branch: 'main', credentialsId: 'from_jenkinsfile', url: 'https://github.com/ManithejaCyberark/building-a-multibranch-pipeline-project.git'
    echo "completed"
   }
  echo "completed"
 }
 
//  stage('checkout'){
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
