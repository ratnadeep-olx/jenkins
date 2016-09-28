node('master') {
    stage('fetch'){
      echo 'fetching from git'  
git credentialsId: 'c483942c-4cee-4d25-97a6-238273657c5f', url: 'git@github.com:naspersclassifieds-regional/olxsa-atlas-web-env-test.git'    }
    stage('composer'){
        echo 'composer update...'
        sh 'composer self-update'
        sh 'composer update -o --no-dev'
        echo 'NPM install....'
        sh 'npm install --production'
        echo 'Gulp'
        sh 'node_modules/gulp/bin/gulp.js'
    }
}
