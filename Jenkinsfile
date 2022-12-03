 pipeline{
    agent : any
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
                bat("npm run build")
                echo "hello sir i am deploying your app on server"
            }
        }
    }
 }
