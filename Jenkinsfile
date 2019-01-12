pipeline {
    agent any
    stages {
        stage ('SCM') {
            steps {    git 'https://github.com/pandian3k/Maven-Demo.git' }
            
        }
    stage ('BUILD') {
            steps {     bat 'mvn clean'
                         bat 'mvn install'
                     }
            
                  }
    
    stage ('Deployment') {
            steps {    bat 'xcopy /y "C:\\Program Files (x86)\\Jenkins\\workspace\\demo_pipeline_4\\multi-module\\webapp\\target\\webapp.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"'
            }
            
        }
    }
    }



