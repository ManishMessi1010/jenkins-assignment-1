
pipeline {
    agent {
        label 'linux-agent'
    }

    triggers {
        // GitHub webhook will trigger this pipeline
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh '''
                    echo "Build triggered by GitHub webhook!"
                    echo "Repository: jenkins-assignment-1"
                    hostname
                    whoami
                    git --version
                    java -version
                '''
            }
        }

        stage('Success') {
            steps {
                echo 'CI Pipeline completed successfully!'
            }
        }
    }
}
