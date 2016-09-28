node('master') {
    stage('fetch'){
      echo 'fetching from git'  
      git credentialsId: '4e43c885-b63e-4c75-bfc1-818900e037e7', url: 'https://github.com/naspersclassifieds-regional/olxsa-atlas-web-env-test.git'
    }
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
