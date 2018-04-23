pipeline {
  agent {
    docker {
      image 'us.gcr.io/fred-hsu-veos/ceos-lab'
      args '''--name=ceos --privileged -e CEOS=1 -e container=docker
-e EOS_PLATFORM=Docker -e SKIP_ZEROTOUCH_BARRIER_IN_SYSDBINIT=1 -e ETBA=1 -e
INTFTYPE=eth '''
    }

  }
  stages {
    stage('stage-1') {
      steps {
        echo 'Hello world!'
        sh 'docker run us.gcr.io/fred-hsu-veos/ceos-lab /sbin/init'
      }
    }
  }
}