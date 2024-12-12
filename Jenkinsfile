pipeline {
    agent any

    stages {
        stage('Build_stage_windows') {
            steps {
                bat '''
                    echo Starting Build Process
                    dir
                    node --version
                    npm --version
                    echo Installing dependencies...
                    npm ci
                    echo Building the project...
                    npm run build
                    dir
                '''
            }
        }
    }
}
