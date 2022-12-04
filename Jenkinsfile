 pipeline{
    agent any
  environment{
    MY_PATH = "C:/Program Files/apache-tomcat-10.0.27-windows-x64/apache-tomcat-10.0.27/webapps"
  }
  tools{
   nodejs "NODEJS"
  }
    stages{
        stage("build"){
            steps{
                bat("node -v")
                echo "hello sir i am jenkinsfile"
                bat("npm install")
                echo "build done sir"
            }
        }
        stage("test"){
            steps{
                echo "hello sir i am testing your code, which is looking trash as of now"
            }
        }
        stage("deploy"){
            steps{
//                 bat("npm run build")
             bat("cd ${MY_PATH}")
                bat("mkdir ReactApp")
                echo "hello sir i am deploying your app on server"
            }
        }
    }
 }
