pipeline {
    agent none

    stages {

        stage ('Build war and put it to container'){
              agent {
                    docker {
                    args '-u root -v /var/run/docker.sock:/var/run/docker.sock'
                    image 'build_war:v2.0'
                    registryCredentialsId 'dc917212-dd0b-45fc-ac76-ef4cf0256eb2'
                    registryUrl 'http://20.113.35.233:8123'
                     }
                    }
              steps {
                     git 'https://github.com/lolipopser/boxf.git'
                     sh 'mvn package'
                    }

        }

    }

}