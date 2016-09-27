node('master') {
    stage('fetch') {
      git url: 'https://github.com/naspersclassifieds-regional/olxsa-atlas-web-env-test'
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
