node {
    docker.image('node:lts-buster-slim').inside('-p 3000:3000') {
        env.CI = 'true'
        stage('Build') {
            sh 'npm install'
        }
        stage('Test') {
             sh './jenkins/scripts/test.sh'
        }
    }
}