node{
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
   echo "connecting to git server"
  withCredentials([conjurSecretUsername(credentialsId: 'b52289d4-94f4-4f88-843f-87df276915a2', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
     git branch: 'master', credentialsId: 'b52289d4-94f4-4f88-843f-87df276915a2', url: 'https://github.com/ManithejaCyberark/building-a-multibranch-pipeline-project.git'
   echo "$CONJUR_SECRET"
   echo "$b52289d4-94f4-4f88-843f-87df276915a2"
 }
 }
  
//  stage('checkout'){
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
