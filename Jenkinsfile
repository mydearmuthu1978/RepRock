pipeline {
         agent any
         def gitCredId = 'mydearmuthu1978'
         stages {
                 stage('checkout'){
                 steps {
                     script{
                          checkout([
                            $class: 'GitSCM', 
                            branches: [[name: '*/master']], 
                            doGenerateSubmoduleConfigurations: false, 
                            extensions: [[$class: 'CleanCheckout']], 
                            submoduleCfg: [], 
                            userRemoteConfigs: [[credentialsId: '<gitCredentials>', url: '<gitRepo>']]
                        ])
                     }
                 }

                 }
                 stage('Build') {
                 steps {
                     echo 'Hi, GeekFlare. Starting to build the App.'
                 }
                 }
                 stage('Test') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Deploy') {
                 parallel { 
                            stage('Deploy start ') {
                           steps {
                                echo "Start the deploy .."
                           } 
                           }                            
                           }
                           }                
}
}
