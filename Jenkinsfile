pipeline{
    agent any
    stages{
        stage("manual"){
            steps{
               withCredentials([conjurSecretCredential(credentialsId: 'private_key', variable: 'CONJUR_SECRET')]) {
                       sh "echo $CONJUR_SECRET | base64"
                 }
             }
         }
     }
}
