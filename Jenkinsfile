node() {
    stage('Download code from Git') 
               {
    git branch: 'dev', url: 'https://github.com/ash09-SaaS/dec16-code.git'
               }
    stage('Convert into artifact') 
               {
    sh 'mvn package'
               }
    
       }
