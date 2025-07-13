pipeline {
    agent any

    stages {
        stage('Build') {
            agent{
                docker{
                    image 'node:18-alpine'
                }
            }
            steps {
                echo 'Building Project'
                sh '''
                    ls -la
                    node -v
                    npm -v
                    npm ci
                    npm run build
                    ls -la
                '''
                
            }
        }

        stage("Test"){
            steps{
                echo "====++++executing Test++++===="
                sh "test -f build/index.html"
            }
        }
        
    }
}
