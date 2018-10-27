django('django') {
    currentBuild.result = "SUCCESS"

    try {

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

    catch (err) {

        currentBuild.result = "FAILURE"

        echo 'Error Build docker o Push heroku'
       
        throw err
    }

}