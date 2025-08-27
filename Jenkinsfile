
pipeline {
    agent { node { label 'Agent-1' } }
    stages {
        stage('Build') { 
            steps {
                echo 'Building..'
                sh '''
                  ls -ltr
                  pwd
                    echo "Hello World"
                    echo "This is my first Jenkins Pipeline"
                    echo "Learning Jenkins Pipeline"
                '''
            }
        }
        stage('Test') { 
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') { 
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
    }
}