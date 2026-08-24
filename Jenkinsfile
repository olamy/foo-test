pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'mvn clean -B package'                
                }
            }
        }
    }
    /*post {
        failure {
              aiPrompt(
                  prompt: 'Who Am I in jenkins-mcp and why the current job is failing? Can you propose a fix',
                  llmProvider: 'bedrock',
                  mcpServers: ['jenkins-mcp'])
        }
    }*/
}
