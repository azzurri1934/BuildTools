pipeline {
    agent any
    parameters {
        string(name: 'version', defaultValue: 'latest', description: 'ビルドするspigotのバージョンを指定する。')
    }
    stages {
        stage('build'){
            steps {
                //cleanWs()
                sh 'BuildTools.sh $version'
            }
        }
    }
}
