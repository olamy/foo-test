pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'mvn clean package'                
                }
            }
        }
    }
    post {
        failure {
              aiPrompt(
                  prompt: 'Who Am I in jenkins-mcp and why this build is failing? Can you propose a fix',
                  llmProvider: 'bedrock',,
                  mcpServers: ['jenkins-mcp'])
        }
    }
}
