pipeline{
    agent any

    stages {
        stage('Build_stage_windows') {
            steps {
                bat '''
                    npm audit fix --force
                    echo Installing dependencies...
                    npm ci
                    echo Building the project...
                    npm run build
                    dir
                '''
            }
        }

        stage('Test_Windows') {
            steps {
                bat '''
                      IF EXIST build\\index.html (
                           echo "build/index.html exists."
                     ) ELSE (
                           echo "build/index.html does not exist."
                        )
                    '''
            }
        }
    }
}
