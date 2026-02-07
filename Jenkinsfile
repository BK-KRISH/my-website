pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/BK-KRISH/my-website.git'
            }
        }

        stage('Deploy Website') {
            steps {
                bat '''
                if exist C:\\web-deploy (
                    rmdir /s /q C:\\web-deploy
                )
                mkdir C:\\web-deploy
                xcopy * C:\\web-deploy /E /H /C /I
                '''
            }
        }
    }
}
