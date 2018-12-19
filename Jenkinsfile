pipeline {
    agent any
//    options {
//        buildDiscarder(logRotator(daysToKeepStr: '31', artifactNumToKeepStr: '5'))
//    }
    parameters {
        string(name: 'version', defaultValue: 'latest', description: 'ビルドするspigotのバージョンを指定する。')
    }
    stages {
        stage('build'){
            steps {
                //cleanWs()
                sh './BuildTools.sh $version'
            }
        }
    }
//    post {
//        success {
//            cleanWs()
//        }
//    }
}
