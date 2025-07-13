pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
                sh ```
                    ls -la
                    node -v
                    npm -v
                    npm ci
                    npm run build
                    ls-la
                ```
                
            }
        }
        
    }
}
