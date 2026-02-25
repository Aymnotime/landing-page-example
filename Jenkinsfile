pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'git@github.com:Aymnotime/landing-page-example.git'
            }
        }

        stage('Build') {
            steps {
                sh 'ls -la'
                echo 'hello world'
            }
        }

        stage('Deploy') {
            steps {
                sshagent(['Thesecretjungle']) {
                    sh 'scp index.html aymen-galaxy@ssh-aymen-galaxy.alwaysdata.net:/home/aymen-galaxy/www/'
                }
            }
        }
    }
}
