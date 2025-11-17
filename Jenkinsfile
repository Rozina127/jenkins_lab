pipeline {
    environment { 
        VERSION = '1.0' // Yeh naya block add kiya hai
    }
    agent any
    stages {
        stage('Build') {
            steps {
                // Pehle yahan sirf 'Building..' tha
                echo "Building Version ${env.VERSION}" // Is line ko tabdeel kiya hai
            }
        }
        stage('Test') {
            when {
                branch 'main'
            }
            steps {
                echo 'Testing..'
                // Here you can define commands for your tests
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // Here you can define commands for your deployment
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully'
        }
    }
}
