node {
    /* Scripted Pipeline */
    docker.image('node:lts-bullseye-slim').inside {
        stage('Build') {
            checkout scm
            sh 'npm install'
        }

        stage('Test') {
            checkout scm
            sh './jenkins/scripts/test.sh'
        }
    }
}
