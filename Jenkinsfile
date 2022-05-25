node{

    stage('SCM Checkout')
    {
        git credentialsId: '797bcbfe-384c-42da-ab0b-49bf9464bd5d', url: 'https://github.com/Yougeshdhomeja/DevOps-Project.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
   stage('PUSH image to Docker Hub')
    {
        withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u yougeshdhomeja -p 'yougesh12++' "
        }
        sh 'docker push yougeshdhomeja/devops'
    }
