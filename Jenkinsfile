pipeline {
    agent { label 'windows' }
    stages {
        stage('Building Microservices') {
            steps {
                bat '''
                for /d %i in (*) do (
                  cd %i
                  echo "Building %i"
                  docker build -t %i .
                  cd ..
                )
                '''
            }
        }
    }
}
