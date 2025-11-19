pipeline {
  agent any

  stages {
    stage('Build & Test') {
      steps {
        bat 'mvn clean verify'
      }
    }

    stage('Report') {
      steps {
        publishHTML(
          [ reportDir: 'target/site/serenity',
            reportFiles: 'index.html',
            reportName: 'Serenity Report'
          ]
        )
      }
    }
  }
}
