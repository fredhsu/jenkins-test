pipeline {
  agent any
  stages {
    stage('stage-1') {
      steps {
        echo 'Hello world!'
      }
    }
    stage('run ceos') {
      steps {
        sh 'gcloud docker -- pull us.gcr.io/fred-hsu-veos/ceos-lab:latest'
      }
    }
  }
}