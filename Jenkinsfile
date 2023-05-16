pipeline{
    // agent {label 'linux_agent_1'}
    agent any
    stages{
        stage("manual"){
            steps{
//                 withCredentials([conjurSecretCredential(credentialsId: 'db_password', variable: 'CONJUR_SECRET')]) {
//                        sh 'echo $CONJUR_SECRET | base64'
//                     }
               withCredentials([conjurSecretCredential(credentialsId: 'private_key', variable: 'CONJUR_SECRET')]) {
                       sh "echo $CONJUR_SECRET | base64"
                    }
            }
        }
    }
}
