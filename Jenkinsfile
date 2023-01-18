node{
 stage('git checkout'){
     echo "git checkout"
  }
  stage('build code'){
     echo "create package"
  }
 stage('git server'){
   echo "connecting to git server"
  withCredentials([conjurSecretCredential(credentialsId: 'jenkins-app/db_password_globel_level', variable: 'CONJUR_SECRET')])  {
     git branch: 'master', credentialsId: 'jenkins-app/db_password_globel_level', url: 'https://github.com/ManithejaCyberark/building-a-multibranch-pipeline-project.git'
   echo "conjur secrets value: $CONJUR_SECRET"
 }
 }
  
//  stage('checkout'){
//    git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
//   }
}
