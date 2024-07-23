pipeline {
    agent any
    parameters {
         choice choices: ['dev', 'qa', 'prod'], description: 'choose the environnement where you want to deploy', name: 'environnement'
    }  

    stages {
        stage('deploy to dev') {

            when {
              expression {
               params.Environment == "dev"
              }
            }
            steps {
                echo 'Hello World out'
            }
        }
    
    
        stage('test to qa') {
            when {
              expression {
               params.Environment == "qa"
              }
            }
            steps {
                echo 'Hello deploy to qa'
            }
        }
    

        stage('deploy to prod') {
            when {
              expression {
               params.Environment == "prod"
              }
            }
            steps {
                echo 'Hello deploy to prod'
            }
        }
    }

    

}
