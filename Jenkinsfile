node {
  def app

  stage('Clone repository'){
    checkout scm


  }

  stage('Build image'){
    app = docker.build("melaen/pipeline1")


  }

  stage('Push image'){
    docker.withRegistry('https://registry.hub.docker.com','docker-hub-credentials'){
      app.push("latest")
    }

  }
}
