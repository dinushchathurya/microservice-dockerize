pipeline {
   agent any
   stages {
      stage('Building Microservices') {
         steps {
            bat '''
               for /d %%i in (*) do (
                  cd %%i
                  echo "Building %%i"
                  docker build -t %%i:1.0.0 .
                  cd .. 
               )
            '''
         }
      }
   }
}
