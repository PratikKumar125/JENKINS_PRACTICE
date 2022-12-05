 pipeline{
    agent any
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
                echo 'dockerhub uname is %DOCKER_CREDS_USR%'
                
                echo "hello sir i am testing your code, which is looking trash as of now"
            }
        }
        stage("deploy"){
             environment{
                 DOCKER_CREDS = credentials("dockerhub")
             }
             steps{
                bat("docker logout")
                bat("docker login -u ${DOCKER_CREDS_USR} -p ${DOCKER_CREDS_PSW}')
//              bat("docker push pratikkumar378/myreactappnew")
                echo "image pushed successfully"
            }
        }
    }
 }
