pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               git branch: 'main',
               url: 'https://github.com/HrishiPreetham/PES1UG21CS236_Jenkins.git' 
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG21CS236-1'
                sh 'g++ newfile.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './non_existent_script.sh'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
