pipeline{
    agent any
    stages{
        stage("checkout stge"){
            steps{
                git url:'https://github.com/pabitrakumarsamal/jenkinRepo1.git',branch:'main'
            }
        }
        stage("create image"){
            steps{
                sh 'docker build -t myimage111 .'
            }
        }
        stage("create container"){
            steps{
                sh 'docker run -d -p 3501:3501 myimage111'
            }
        }
    }
}