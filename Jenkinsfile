pipeline {
    agent any
    parameters{
        choice(name:'VERSION',choices :['1.1.0','1.2.0','1.3.0'])
        booleanParam(name:'ExecuteTest',defaultValue:true,description:'')
    }
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
                    env.BRANCH_NAME == 'dev' 
                }
            }
            when{
                expression{
                    params.ExecuteTest == true
                }
            }
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                echo "deploying version ${params.VERSION}"
            }
        }
    }
    post {
        always{
            echo "always" 
        }
        success{
            echo "sucsess" 
        }
        failure{
            echo "always fails" 
        }
    }
}
