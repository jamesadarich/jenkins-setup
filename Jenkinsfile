node {
    sleep 60
    
    docker.image('node:8.6.0').inside('-u root -v /var/run/docker.sock:/var/run/docker.sock -v /usr/bin/docker:/usr/bin/docker') {
        stage('Setup') {
            checkout scm
        }
        
        stage('Build Containers') {
            docker.build("jamesadarich/jenkins-master:latest", "./docker-images/master")
        }
    }
}
