node {
    stage('Download git code from github') {
    git branch: 'dev', url: 'https://github.com/clouddevopseng/Firstjobcode.git'
     }
     stage('Convert into artifacts') {
    sh 'mvn package'
     }
     stage('Deploy') {
     deploy adapters: [tomcat9(credentialsId: 'dev', path: '', url: 'http://172.31.8.113:8080')], contextPath: '/dev-new-17-04', war: '**/*.war'
     }
}
