pipeline {
   agent any
   stages {
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
