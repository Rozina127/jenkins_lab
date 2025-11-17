pipeline {
    environment { 
        VERSION = '1.0' 
    }
    agent any
    tools {
        maven 'Maven' // Yeh naya block add kiya hai. 'Maven' woh naam hai jo aap ne Jenkins Tools mein set kiya hai.
    }
    stages {
        stage('Build') {
            steps {
                echo "Building Version ${env.VERSION}" 
                
                // Yeh Windows ke liye 'bat' command hai
                bat 'mvn --version' // Yeh line add ki hai
            }
        }
        stage('Test') {
            when {
                branch 'main'
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
