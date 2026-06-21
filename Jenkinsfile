pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'echo Building Maven Project'
                bat 'mvn clean package'
            }
        }

        stage('Deploy') {
            steps {
                bat 'wsl ansible-playbook -i inventory deploy.yml'
            }
        }

    }
}