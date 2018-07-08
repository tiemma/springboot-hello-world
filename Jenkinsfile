pipeline {

   agent any    

    stages {
        stage('Build Package and Image') {
        /*
        I used the dockerfile-maven-plugin from spotify
        so my build process for maven would build the
        image and push it automatically without any other
        configurations
        */
            steps {
                sh 'mvn -B -DskipTests  clean package'
            }
        }
    }
}
