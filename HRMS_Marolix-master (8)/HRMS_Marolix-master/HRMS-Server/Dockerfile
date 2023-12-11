pipeline {
agent any 

    environment {
        PATH = "/path/to/pyenv/bin:${env.PATH}"
        SHELL = '/bin/bash' // or '/bin/sh' depending on your shell
    }







stages{


stage("intigration"){

steps{
git branch: 'main', url: 'https://github.com/R807989/hrmsnew.git'

}

}


  

 
           stage('install python depencies') {
            steps {
                script {
                    // Install dependencies using Pipenv
                    sh 'pipenv install --dev'
                }
            }
        }

 

 stage('Build Docker Image') {
            steps {
        dir("/var/lib/jenkins/workspace/python/HRMS-Server") {

                script {
                    // Build Docker image
                   
sh 'docker build -t python .'
                }
            }
        }
}
 stage('deploy') {
            steps {
                script {
                    // Run Docker container with environment variables
                    sh 'docker run --name my-python-container -d -p 8000:8000 -e EMAIL_HOST_USER=myuser -e OTHER_VARIABLE=value python'
                }
            }
        }
           

            
        
    





}
}


GitHub - R807989/hrmsnew
https://github.com
