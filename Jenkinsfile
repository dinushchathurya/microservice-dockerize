pipeline {
   agent any
   stages {
      stage('Building Microservices') {
         steps {
            bat '''
               // for /d %%i in (*) do (
               //    cd %%i
               //    echo "Building %%i"
               //    docker build -t %%i .
               //    cd .. 
               // )
               
                  set "k8s_dir=%cd%"
                  call %k8s_dir%\run.bat

                  set "services=%SPLIT_SERVICES:-%SERVICES:-""%"
            '''
         }
      }
   }
}
