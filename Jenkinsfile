@Library("Jenkins-13") _

pipeline {
    agent any
    stages {
        stage("Demo") {
            steps {
                script("priyanka")
            }
        }
      
    }  
    post {
        always {
            echo 'Test run completed'
        }
        success {
            echo 'Successfully!'
        }
        failure {
            echo 'Failed!'
        }
    }
}
