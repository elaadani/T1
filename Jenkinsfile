pipeline {

	agent any

	 stages {
    
	    stage('Test'){

	         print "Comprobando la instalación de git"

	         sh 'git -v'

	       }

	       stage('Pull desde el repositorio git'){

	          sh './PullGit.sh'

	       }

	       stage('Construyendo una imagen de docker'){

	          sh './DockerBuild.sh'
	       }

	       stage('Deploy'){

	         echo 'Push hacia Heroku'
	         sh './DockerPushHeroku.sh'

	       }
	   }




}