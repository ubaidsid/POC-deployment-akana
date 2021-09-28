pipeline {
    agent any
    stages {
        stage('deployment') {
            steps {
                sh("curl -X POST -H 'Content-Type: application/json' -H 'Accept: application/json' -i -k 'https://preprod-portal-entapi.spectrummobile.com/api/login' --data '{
  "email":"ubaid.urrehman@infosys.com",
  "password":"@Kashu11223344!",
  "federationLogins":true
}'")
                echo "Deploying on Dev ..."
            }
        }
        stage('Test cases') {
            steps {
                echo "Sanity Test on Dev .."
            }
        }
    }
}
