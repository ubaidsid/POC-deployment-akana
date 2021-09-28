pipeline {
    agent any
    parameters {
    string(name: 'STATEMENT', defaultValue: 'hello; ls /', description: 'What should I say?')
  }
  stages {
    stage('Example') {
      steps {
        /* CORRECT */
        sh('echo ${STATEMENT}')
      }
    }
  }
        stage('Test cases') {
            steps {
                echo "Sanity Test on Dev .."
            }
        }
    }
}
