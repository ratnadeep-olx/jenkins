node('master') {
    stage('fetch') {
      echo 'fetching from git'  
      git credentialsId: 'c4c7beda-5d61-4b22-82b7-79b4e487ab1a', url: 'https://github.com/naspersclassifieds-regional/olxsa-atlas-web-env-test'
    }
    stage ('composer') {
        echo 'Building....'
    }
}
