pipeline {
    agent any
    stages {
        stage('deployment') {
            steps {
                curl --location --request POST -k 'https://preprod-portal-entapi.spectrummobile.com/api/login' \
--header 'Authorization: Basic dWJhaWQudXJyZWhtYW5AaW5mb3N5cy5jb206QEthc2h1MTEyMjMzNDQh' \
--header 'Content-Type: application/json' \
--data-raw '{
  "email":"ubaid.urrehman@infosys.com",
  "password":"@Kashu11223344!",
  "federationLogins":true
}'
                
            }
        }
        stage('Test cases') {
            steps {
                echo "Sanity Test on Dev .."
            }
        }
    }
}
