pipeline {
   agent any
   stages {
      stage('Checkout Source') {
         steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/dinushchathurya/microservice-dockerize.git']]])
         }
      }
      stage('Building Microservices') {
         steps {
            sh '''
               for dir in */; do
                  cd $dir
                  echo "Building $dir"
                  docker build -t $dir .
                  cd ..
               done
            '''
         }
      }
   }
}
