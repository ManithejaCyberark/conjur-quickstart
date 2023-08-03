pipeline{
    agent any
    stages{
        stage("Dev-Team-1 Credentials"){
            steps{
                withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET_TEST_PIPELINE')]) {
                  sh 'echo $CONJUR_SECRET_TEST_PIPELINE | base64'
                }
            }
        }
        stage("Test-pipeline credentials"){
            steps{
                withCredentials([conjurSecretCredential(credentialsId: 'Dev-Team-1', variable: 'CONJUR_SECRET_DEV_TEAM')]) {
                  sh 'echo $CONJUR_SECRET_DEV_TEAM | base64'
                }
            }
        }
    }
}
