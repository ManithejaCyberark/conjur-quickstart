pipeline{  
   agent any 
    stages{
         stage("git checkout"){
             steps{
                 echo "cloned the code from git repo"
             }
         }     
      stage("test credentials"){
           steps{
             withCredentials([conjurSecretCredential(credentialsId: 'private_key', variable: 'CONJUR_SECRET')]) {
               sh "echo $CONJUR_SECRET | base64"
                  }
              }
          }
      }
}
