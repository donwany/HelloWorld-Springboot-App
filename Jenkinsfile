pipeline{
    agent any
    stages{
        stage('Git clone'){
            steps{
                git 'https://github.com/donwany/HelloWorld-Springboot-App.git'
            }
        }
        
        stage('maven build'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Create Dockerimage'){
            steps{
                sh 'docker build -t worldbosskafka/springboot:latest .'
            }
        }
        
         stage('Completed'){
            steps{
                echo 'Build completed successfully ...'
            }
        }
        
    }
}
