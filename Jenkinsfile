node('master') {
    stage('fetch') {
      git credentialsId: 'c4c7beda-5d61-4b22-82b7-79b4e487ab1a', url: 'https://github.com/naspersclassifieds-regional/olxsa-atlas-web-env-test'
      def v = version()
      if (v) {
        echo "Building version ${v}"
      }
    }
    stage ('composer') {
        echo 'Building....'
    }
}
def version() {
  def matcher = readFile('pom.xml') =~ '<version>(.+)</version>'
  matcher ? matcher[0][1] : null
}
