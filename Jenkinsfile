pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'echo Building Maven Project'
                
            }
        }

        stage('Deploy') {
            steps {
                bat 'wsl ansible-playbook -i inventory deploy.yml'
            }
        }

    }
}
