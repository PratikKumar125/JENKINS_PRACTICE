 pipeline{
    agent any
    environment{
       DOCKER_CREDS = credentials("dockerhub")
//     MY_PATH = "C:/Program Files/apache-tomcat-10.0.27-windows-x64/apache-tomcat-10.0.27/webapps"
  }
//   tools{
//    nodejs "NODEJS"
//   }
    stages{
        stage("build"){
            steps{
//              bat("node -v")
                echo "hello sir i am jenkinsfile"
//              bat("npm install")
                bat("docker build -t pratikkumar378/myreactappnew .")
                echo "build done sir"
            }
        }
        stage("test"){
            steps{
                echo "dockerhub uname is ${DOCKER_CREDS_USR}"
                
                echo "hello sir i am testing your code, which is looking trash as of now"
            }
        }
        stage("deploy"){
            steps{
             bat("docker logout")
             bat('docker login -u $DOCKER_CREDS_USR -p $DOCKER_CREDS_PSW')
             bat("docker push pratikkumar378/myreactappnew")
             echo "image pushed successfully"
            }
        }
    }
 }
