pipeline {
    agent any

    stages {
        stage('Build_stage_windows') {
            steps {
                bat '''
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
