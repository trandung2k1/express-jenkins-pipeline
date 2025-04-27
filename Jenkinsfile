pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/trandung2k1/express-jenkins-pipeline.git'
            }
        }
        stage('Test PowerShell') {
            steps {
                powershell '''
                Write-Host "This is a PowerShell script running on Windows"
                docker --version
                '''
            }
        }
        // stage('Build and push image') {
        //     steps {
        //         // This step should not normally be used in your script. Consult the inline help for details.
        //         withDockerRegistry(credentialsId: 'express-jenkins-pipeline', url: 'https://index.docker.io/v1/') {
        //             sh 'docker version'
        //             // sh 'docker build -t trandung2001/express-jenkins-pipeline .'
        //             // sh 'docker push trandung2001/express-jenkins-pipeline'
        //         }
        //     }
        // }
    }
}