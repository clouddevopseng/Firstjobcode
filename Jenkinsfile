node {
    stage('Download git code from github') {
    git branch: 'test', url: 'https://github.com/clouddevopseng/Firstjobcode.git'
     }
     stage('Convert into artifacts') {
    sh 'mvn package'
     }
     stage('Deploy') {
     deploy adapters: [tomcat9(credentialsId: 'test', path: '', url: 'http://172.31.14.12:8080')], contextPath: '/test-new-17-04', war: '**/*.war'
     }
}
