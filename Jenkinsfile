node() {
    stage('Download code from Git') 
               {
    git branch: 'dev', url: 'https://github.com/ash09-SaaS/dec16-code.git'
               }
    stage('Convert into artifact') 
               {
    sh 'mvn package'
               }
    stage('Deploy on tomcat server') 
               {
    deploy adapters: [tomcat9(credentialsId: '6eb9749c-44a7-4b93-9096-cd8188e0d76e', path: '', url: 'http://3.101.53.109:8080/')], contextPath: '/jenkinsdevapp', war: '**/*.war'
               }
       }
