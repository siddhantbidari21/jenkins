pipeline {
     agent {
          label 'slave'
     }
    
    environment {
        GIT_REPO_URL = 'https://github.com/siddhantbidari21/jenkins'
        MAVEN_TOOL = 'Maven'
    }
    
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', 
                          branches: [[name: '*/master']], 
                          userRemoteConfigs: [[url: env.GIT_REPO_URL]]])
            }
        }
    }
}
