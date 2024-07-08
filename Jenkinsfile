pipeline {
  agent any

  tools {nodejs "{your_nodejs_configured_tool_name}"}

  stages {
    stage('Install Postman CLI') {
      steps {
        sh 'curl -o- "https://dl-cli.pstmn.io/install/linux64.sh" | sh'
      }
    }

    stage('Postman CLI Login') {
      steps {
        sh 'postman login --with-api-key $POSTMAN_API_KEY'
        }
    }

    stage('Running collection') {
      steps {
        sh 'postman collection run "33605373-ac933618-1fa0-4d33-800b-96352e29e0d4"-e "33605373-e5dab369-3b4a-49a5-9f70-7b3f9d3146fb"'
      }
    }
  }
}
