pipeline{
    agent any
    stages{
        stage("checkout stge"){
            step{
                git url:'https://github.com/pabitrakumarsamal/jenkinRepo1.git',branch:'main'
            }
        }
        stage("create image"){
            step{
                sh 'docker build -t myimage111 .'
            }
        }
        stage("create container"){
            step{
                sh 'docker run -d -p 3501:3501 myimage111'
            }
        }
    }
}