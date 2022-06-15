pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo 'Running ${env.BUILD_ID} on ${env.JENKINS_URL}'
            }
        }
        stage('Test') {
            when{
                expression{
                    env.BRANCH_NAME == 'Dev' || env.BRANCH_NAME == 'main'
                }
            }
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
        always{
            // always 
        }
        success{
            // sucsess 
        }
        failure{
            // always 
        }
    }
}
