pipeline {
    agent any 
    stages {
        stage("build"){
            steps {
                script {
            sh """
            aws ecr get-login-password --region eu-north-1 | sudo docker login --username AWS --password-stdin 315073111691.dkr.ecr.eu-north-1.amazonaws.com
            sudo docker build -t 315073111691.dkr.ecr.eu-north-1.amazonaws.com/frontend:latest .
            sudo docker push 315073111691.dkr.ecr.eu-north-1.amazonaws.com/frontend:latest

            """
        }
         }
    }
}
}
