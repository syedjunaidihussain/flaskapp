pipeline{
    agent any
        stages{
            stage('Clone'){
                steps{
                    git branch: 'main', url: 'https://github.com/syedjunaidihussain/flaskapp.git'
                }
            }
            
            stage('Build'){
                steps{
                    sh 'sudo docker build -t flaskapp:latest .'                    
                }
            }
            
            stage('Deploy'){
                steps{
                    sh 'sudo docker run -d --name flaskcontainer -p 5000:5000 flaskapp'
                }
            
            }
        }
    }

