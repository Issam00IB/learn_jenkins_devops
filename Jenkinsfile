pipeline {
    agent any

    stages {
        stage('Build_stage_windows') {
            steps {
                bat '''
                    dir
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    dir
                '''
            }
        }
    }
}
