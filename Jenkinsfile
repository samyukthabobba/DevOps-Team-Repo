pipeline {
    agent any

    stages {
        stage('Git Cloning') {
            steps {
                git 'https://github.com/samyukthabobba/Development-Team-Repo.git'
            }
        }
        stage('Build Application Code') {
            steps {
                sh 'mvn package -f pom.xml'
            }
        }
         
      stage('Deploy Code In Tomcat Dev Server-1') {
            steps {
               sh 'cp target/*.war /home/jenkins/apache-tomcat-8.5.82/webapps'
            }
        }
    
    }
 
}
