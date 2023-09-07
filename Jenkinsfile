pipeline {
     agent {
          label 'slave'
     }
    
    environment {
        GIT_REPO_URL = 'https://github.com/prane12/devops'
        MAVEN_TOOL = 'M3'
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
