pipeline {
    agent any
    stages{
        stage(scm){
            steps{
                git 'https://github.com/doddisairam/spring-petclinic.git'
            }
        }
        
        stage(build){
            steps{
                sh '''
                mvn clean install
                '''
            }
        }

        stage(imagebuild){
            steps{
                sh '''
                docker build -t srini-test .
                '''
            }
        }
    }
}
 
