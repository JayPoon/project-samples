pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        
        // This step should not normally be used in your script. Consult the inline help for details.
        withDockerServer([uri: 'registry.cn-hangzhou.aliyuncs.com']) {
            sh '''cd containerization-spring-with-helm
docker build -t registry.cn-hangzhou.aliyuncs.com/k8s-mirrors/spring-sample .'''
        sh '''docker push registry.cn-hangzhou.aliyuncs.com/k8s-mirrors/spring-sample'''
        }
      }
    }
  }
}
