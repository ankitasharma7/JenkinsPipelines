pipeline {

    agent any
    stages {

        stage('checkout codebase'){
            steps(
                checkout scm: [$class: 'GITSCM' ,userRemoteConfigs: [[credentialsId: 'jenkind-github',url: 'git@github.com:ankitasharma7/multithreading-example-1.git']]]
            )
        }

        stage('Build'){
            steps (
                sh 'gcc mt-example-0.c -lpthread'
            )
        }

        stage('Test'){
            steps (
                sh './a.out'
            )
        }

        stage('Deploy') {
            steps(
                sh 'echo Done!'
            )
        }
    }
}
