pipeline {
  agent any
  stages {
    stage('GitPull') {
      steps {
        git(url: 'https://github.com/avinashdesireddy/dockerfiles.git', branch: 'master', poll: true, changelog: true)
      }
    }
    stage('Build Image') {
      steps {
        sh '''cd ansible
docker build -t dtr.avinash.dockerps.io/docker/ansible:latest .'''
      }
    }
  }
}