pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                echo 'Comprobando la instalación de git..'
                sh 'git --version'
            }
        }
        stage('Pull desde el repositorio git') {
            steps {
                 sh '/bin//PullGit.sh'
            }
        }
        stage('Construyendo una imagen de docker') {
            steps {
                sh '/bin//DockerBuild.sh'
            }
        }
    }
}