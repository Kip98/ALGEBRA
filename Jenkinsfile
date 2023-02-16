pipeline {
  agent any
  stages {
    stage('tool version') {
      steps {
        echo 'checking tools'
        sh '''mvn --version
git --version
java -version'''
      }
    }

    stage('build and test') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('deploy') {
      steps {
        echo 'deployment stage'
      }
    }

  }
}