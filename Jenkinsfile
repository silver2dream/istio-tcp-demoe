pipeline {
  agent any
  stages {
    stage('Checkout') {
      agent any
      steps {
        git(url: 'https://github.com/silver2dream/istio-tcp-demo.git', changelog: true, branch: 'generic_echo')
        telegramSend(message: '"Hello World"', chatId: -598293671)
      }
    }

    stage('Build') {
      steps {
        sh 'go build'
      }
    }

  }
}