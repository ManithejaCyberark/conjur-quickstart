pipeline{
    
    agent any
    stages{
        stage("Dev-Team-credentials"){
            steps{
                 withCredentials([conjurSecretCredential(credentialsId: 'conjur_provided_dev-team-1cred', variable: 'CONJUR_SECRET_DEV_TEAM')])  {
                  sh 'echo $CONJUR_SECRET_DEV_TEAM | base64'
                }
            }
        }
        stage("test-pipeline Credentials"){
            steps{
                withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET_TEST_PIPELINE')]) {
                  sh 'echo $CONJUR_SECRET_TEST_PIPELINE | base64'
                }
            }
        }
    }
}
