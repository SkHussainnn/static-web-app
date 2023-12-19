pipeline {
    agent any

    stages{
        stage("Checkout Code") {
            script {
                echo "Checkout Code started"
                git branch: "main" , url: 'https://github.com/SkHussainnn/static-web-app.git'
                echo "Checkout Code completed"
        stage("Deployment Code") {
           script{
               echo "Deployment Code started"
               sh 'scp -r /var/lib/Jenkins/woekspace/Static-web-app/ * ubuntu@13.212.78.178:/var/www/html/'
               echo "Deployment Code completed"
           }
        }
            }
        }
    }
}