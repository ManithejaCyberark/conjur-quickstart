pipeline{
//    agent any
  
    agent {
    // node { label 'master-Node' } 
    //node {label 'jenkins-slave1'}
      node {label 'slave-2'}
   }
  
    stages{
     stage("git checkout"){
         steps{
             echo "cloned the code from git repo"
         }
     }
 
     stage("print value of conjur secrets"){
         steps{
                echo "passing folder level credentials"
            withCredentials([conjurSecretUsername(credentialsId: 'from_jenins_file_user1_password', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
            echo "secret value of is: $CONJUR_SECRET and $USERNAME"
            //git branch: 'main', credentialsId: 'ManithejaCyberark', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
            echo "completed"  
            }
         }
     }
  }
}
