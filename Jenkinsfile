pipeline {
    agent any

    stages {
        stage("Checkout Code") {
            steps {
                echo "Checkout Code started"
                git branch: "main", url: 'https://github.com/SkHussainnn/static-web-app.git'
                echo "Checkout Code completed"
            }
        }

        stage("Deployment Code") {
            steps {
                echo "Deployment Code started"
                sh 'scp -r /var/lib/jenkins/workspace/Static-web-app/* http://47.128.241.247:/var/www/html/'
                echo "Deployment Code completed"
        stage("Deployment") {
            steps {
                echo "Deployment started"
                deploy adapters: [nginx(url:'http://47.128.241.247:80' , credentialsId: 'nginxcred')]
            }
        }
            }
        }
    }
}
