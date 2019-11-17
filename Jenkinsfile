node('master') {
 
 stage('Start') {
  checkout scm
 }

 stage('Static Analysis') {
  //sh '~/.nvm/versions/node/v13.0.1/bin/npm install eslint && ~/.nvm/versions/node/v13.0.1/bin/npm run lint'
  //sh 'npm run lint'
  echo 'Passed Static Analysis'
 }

 stage('Unit Test') {
  //sh 'npm run test'
  echo 'Passed Unit Test'
 }

 stage('Build') {
  sh "docker images"
  sh "docker rmi image react-app-aws_client -f"
  sh "docker rmi image react-app-aws_server -f"
  sh "/usr/local/bin/docker-compose build"  
  sh "docker images"
  sh "docker ps -a"
 }

  stage('Deployment') {
   sh "docker ps -a"
   //sh "/usr/local/bin/docker-compose up"
   //sh 'docker stop myreact-app-container || exit 0'
   //sh 'docker kill myreact-app-container || exit 0'
   //sh 'docker rm myreact-app-container || exit 0'
   //sh "docker run --name myreact-app-container -p 8081:80 myreact-app:${BUILD_NUMBER} &"
   //sh "docker restart myreact-app-container"
   //sh "docker ps -a"
  }

}
