pipeline {
    agent any
    parameters {
        string(name: 'version', defaultValue: 'latest', description: 'ビルドするspigotのバージョンを指定する。')
    }
    stages {
        stage('build'){
            agent any
            steps {
                //sh '#!/bin/bash -x'
                sh 'curl -o BuildTools.jar https://hub.spigotmc.org/jenkins/job/BuildTools/lastSuccessfulBuild/artifact/target/BuildTools.jar'
                //git config --global --unset core.autocrlf
                sh 'java -Xmx1024M -jar BuildTools.jar --rev $version'
                //sh 'echo "hello"'
                //echo "hello2"
            }
        }
    }
}
