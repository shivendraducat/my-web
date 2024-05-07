pipeline{
    agent any
    stages{
        stage("my first"){
            steps{
                echo "hello my project"
            }
        }
        
        stage("git cloning"){
            steps{
                git url:"https://github.com/shivendraducat/my-web.git" , branch:"main"
            }
        }
        
        stage("docker image"){
            steps{
                sh 'docker build -t my_web1 .'
            }
        }
        
        stage("deploy"){
            steps{
                sh 'docker run -p 80:80 -d my_web1'
            }
        }
    }
}
