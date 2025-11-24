pipeline
{
    agent any
    stages 
    {
        stage('Security Check') 
        {
            steps
            {
                // Retrieving the secret with ID 'my-secret'
                withCredentials([string(credentialsId: 'my-secret', variable: 'API_KEY')])
                {
                    script
                    {
                        echo "Secret found!"
                        // Jenkins automatically masks the secret in the logs
                        echo "The secret is: ${API_KEY}"
                    }
                }
            }
        }
    }
}
