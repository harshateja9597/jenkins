pipeline {
    agent {
        node {
           label 'linux' 
        }
    }
    environment{
        GREETINGS = 'hello jenkins'
    }
    options{
        timeout(time: 1, unit: 'seconds')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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
                sh """
                $GREETINGS
                """
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure{
            echo 'it runs when pipeline fails'
        }
        success{
            echo 'pipeline runs successfully'
        }
    }
}