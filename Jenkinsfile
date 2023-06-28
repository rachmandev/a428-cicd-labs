node {
    docker.image('node:16-buster-slim').inside('-p 3500:3500') {
        
        stage('Build') {
            // sh 'npm config rm proxy'
            // sh 'npm config rm https-proxy --tried removing npm proxy'
            sh 'npm cache clean --force'
            // sh 'npm rm -rf node_modules && rm package-lock.json'
            sh 'npm install -d'
        }

        stage('Test') {
            sh './jenkins/scripts/test.sh'
        }

        // stage('Deploy') {
        //     //
        // }

    }
}