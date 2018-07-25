pipeline {
  /* Declarative Pipeline 
  @autor: Jaime Gaona */
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building ${env.BUILD_NUMBER} with change id: ${env.CHANGE_ID}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Production Deploy') {
            when {
              branch release
            }
            steps {
                echo 'Deploying to stagin'
            }
        }
        stage('Staging Deploy') {
            when {
              branch master
            }
            steps {
                echo 'Deploying to stagin'
            }
        }
    }
}
