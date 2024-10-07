pipeline {
    agent {label 'Slaveubuntu'} 
    stages {

        stage('pull') {
            steps {
                git branch: 'main', url: 'https://github.com/Anuaniyammal/Amazon-Jenkins.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }

    }

  post{

  success{
     echo 'Build success'
  }
    
  failure{
       echo 'Failure in the build'
   }

  }


}
