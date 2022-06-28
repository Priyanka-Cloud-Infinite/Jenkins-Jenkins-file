@Library("Jenkins-13") _

pipeline {
    agent any
    stages {
        stage("Demo") {
            steps {
                welcome("priyanka")
                echo '.....'
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
