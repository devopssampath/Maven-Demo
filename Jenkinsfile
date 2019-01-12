pipeline {
    agent any
    stages {
     stage ('SCM'){ 
         steps {git 'https://github.com/devopssampath/Maven-Demo.git' }
     }
     stage ('BUILD'){ 
         steps { bat 'mvn clean'
                 bat 'mvn install' }
     }
     stage ('DEPLOY'){ 
         steps {bat 'xcopy /y "C:\\Program Files (x86)\\Jenkins\\workspace\\demo_pipe\\multi-module\\webapp\\target\\webapp.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"' }
     }
    }
}
