pipeline {
    agent any
    parameters {
        string(name: 'version', defaultValue: 'latest', description: 'ビルドするspigotのバージョンを指定する。')
    }
    stages {
        stage('build'){
            steps {
                //cleanWs()
                echo $WORKSPACE
                sh 'pwd'
                sh 'BuildTools.sh $version'
            }
        }
    }
}
