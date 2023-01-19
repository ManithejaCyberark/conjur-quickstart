node{
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
  echo "passing folder level credentials"
   withCredentials([conjurSecretUsername(credentialsId: 'd270f370-2106-4eb3-a416-86ec470c7691', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
   echo "$CONJUR_SECRET"
    git branch: 'main', credentialsId: 'd270f370-2106-4eb3-a416-86ec470c7691', url: 'https://github.com/ManithejaCyberark/building-a-multibranch-pipeline-project.git'
    
   }
 }
//  stage('checkout'){
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
