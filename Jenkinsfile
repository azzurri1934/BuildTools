pipeline {
    agent any
    options {
        buildDiscarder(logRotator(daysToKeepStr: '31', artifactNumToKeepStr: '5'))
    }
    parameters {
        string(name: 'version', defaultValue: 'latest', description: 'ビルドするspigotのバージョンを指定する。')
    }
    stages {
        stage('build'){
            steps {
                sh 'chmod 744 ./BuildTools.sh'
                sh './BuildTools.sh $version'
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: spigot-1.13.2.jar, fingerprint: true
        }
        //always {
        //    cleanWs()
        //}
    }
}
