pipeline {
    agent any
    stages {
        stage('deployment') {
           steps {
                echo 'Hello, '

                sh '''#!/bin/bash

                    echo "Hello from bash"
                    echo "Who I'm $SHELL"
                '''
            }
        }
        stage('Test cases') {
            steps {
                echo "Sanity Test on Dev .."
            }
        }
    }
}
