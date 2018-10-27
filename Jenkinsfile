pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                echo 'Comprobando la instalación de git..'
                sh 'git -v'
            }
        }
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