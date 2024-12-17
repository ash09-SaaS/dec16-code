node() {
   stage('Download code from git') 
               {
    git branch: 'dev', url: 'https://github.com/ash09-SaaS/dec16-code.git'
               }
   stage('Convert into Artifact') 
               {
    sh 'mvn package'
               }
   stage('Deploy into cotainer') 
              {
    deploy adapters: [tomcat9(credentialsId: '6eb9749c-44a7-4b93-9096-cd8188e0d76e', path: '', url: 'http://3.101.53.109:8080/')], contextPath: '/jenkinsdevapp', war: '**/*.war'
               }
   }
