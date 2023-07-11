pipeline{

    agent any

    stages{
        stage('Build'){

            steps{
                sh 'sudo docker build -t voting-app ./vote'
                sh 'sudo docker build -t result-app ./result'
                sh 'sudo docker build -t worker ./worker'
                sh 'docker image ls'
            }
        }  

        stage('Run'){
            steps{
                sh 'sudo docker compose -f docker-compose.yml up -d'
            }
        }
    }
}
