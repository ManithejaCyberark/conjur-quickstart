node{
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
  echo "passing folder level credentials"
   withCredentials([conjurSecretCredential(credentialsId: 'efb1ae33-14fd-4cff-ad01-5cf71fc40e67', variable: 'CONJUR_SECRET')])   {
    echo "secret value of is: $CONJUR_SECRET"
    // git branch: 'main', credentialsId: 'efb1ae33-14fd-4cff-ad01-5cf71fc40e67', url: 'https://github.com/ManithejaCyberark/building-a-multibranch-pipeline-project.git'
   }
  echo "completed"
 }
 
//  stage('checkout'){
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
