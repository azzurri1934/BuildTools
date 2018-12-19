pipeline {
    agent any
    parameters {
        string(name: 'version', defaultValue: 'latest', description: 'ビルドするspigotのバージョンを指定する。')
    }
    stages {
        stage('build'){
            steps {
                dir(`$WORKSPACE`) {
                  //cleanWs()
                  sh 'BuildTools.sh $version'
                }
            }
        }
    }
}
