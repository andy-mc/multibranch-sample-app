pipeline {
  agent any
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
    disableConcurrentBuilds()
  }
  stages {
    stage('Hello') {
      steps {
        echo 'oi oi andy !!'
      }
    }
    stage('cat Readme') {
      when {
        branch "fix-*"
      }
      steps {
        sh 'cat README.md'
      }
    }
  }
}
