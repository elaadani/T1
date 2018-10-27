pipeline {
    agent any

    stages {
        
        stage('Pull desde el repositorio git') {
            steps {
                 sh './PullGit.sh'
            }
        }
        stage('Construyendo una imagen de docker') {
            steps {
                sh './DockerBuild.sh'
            }
        }
    }
}