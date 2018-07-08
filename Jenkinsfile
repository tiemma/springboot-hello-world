pipeline {
    /*
    Running this in a docker image to
    unify the build process on any PC
    so there any missing dependencies
    or faulty user configurations.
    */
    agent {
        docker {
            image 'maven:3-alpine'
        }
    }
    stages {
        stage('Build Package and Image') {
        /*
        I used the dockerfile-maven-plugin from spotify
        so my build process for maven would build the
        image and push it automatically without any other
        configurations
        */
            steps {
                sh 'mvn  clean package'
            }
        }
    }
}