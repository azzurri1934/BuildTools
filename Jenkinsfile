pipeline {
    agent none
    parameters {
        string(name: 'version', defaultValue: 'latest', description: 'ビルドするspigotのバージョンを指定する。')
    }
    stages {
        stage('build'){
            steps {
                //sh '#!/bin/bash -x'
                curl -o BuildTools.jar https://hub.spigotmc.org/jenkins/job/BuildTools/lastSuccessfulBuild/artifact/target/BuildTools.jar
                //git config --global --unset core.autocrlf
                //sh 'java -Xmx1024M -jar BuildTools.jar --rev $version'
                echo "hello"
                echo "hello2"
            }
        }
    }
}
