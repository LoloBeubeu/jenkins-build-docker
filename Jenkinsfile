
node {

  
   def IMAGE="srv-web-laurent"
	
    stage('Clone') {
          checkout scm
    }

    stage('Build') {
          docker.build("$IMAGE",  '.')
    }

    stage('Run image') {
        docker.image('srv-web-laurent').withRun('--name ${container_name}' ) { c ->

        sh 'docker ps | grep ${container_name}'
	}

    }
}
