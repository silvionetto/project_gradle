pipeline {
  agent any
  stages {
    stage('Prepare') {
      steps {
        git(url: 'https://github.com/silvionetto/project_gradle.git', branch: 'master', credentialsId: '900b26c3376b6528953c74541f56097e147ab34c', poll: true, changelog: true)
        tool 'Gradle_3_5'
      }
    }
    stage('Build') {
      steps {
        sh 'gradlew build'
      }
    }
  }
}