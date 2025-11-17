pipeline {
    environment { 
        VERSION = '1.0' 
    }
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run the Test stage?') // Yeh naya block add kiya hai
    }
    agent any
    tools {
        maven 'Maven' 
    }
    stages {
        stage('Build') {
            steps {
                echo "Building Version ${env.VERSION}" 
                bat 'mvn --version' 
            }
        }
        stage('Test') {
            when {
                // Pehle yahan 'branch 'main'' tha
                expression { params.executeTests == true } // Is line ko tabdeel kiya hai
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
        success {
            echo 'Pipeline completed successfully'
        }
    }
}
