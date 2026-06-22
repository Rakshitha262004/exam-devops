pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'echo Building Maven Project'
                bat '"C:\Program Files\Java\maven-mvnd-1.0.5-windows-amd64\maven-mvnd-1.0.5-windows-amd64\bin\mvnd.cmd" clean package'
            }
        }

        stage('Deploy') {
            steps {
                bat 'wsl ansible-playbook -i inventory deploy.yml'
            }
        }

    }
}
