pipeline {
    agent any
    stages {
        stage('deployment') {
            steps {
            sh printf '{
  "email":"ubaid.urrehman@infosys.com",
  "password":"@Kashu11223344!",
  "federationLogins":true
}'| http  --follow --timeout 3600 POST 'https://preprod-portal-entapi.spectrummobile.com/api/login' \
 Authorization:'Basic dWJhaWQudXJyZWhtYW5AaW5mb3N5cy5jb206QEthc2h1MTEyMjMzNDQh' \
 Content-Type:'application/json'
            }
        }
        stage('Test cases') {
            steps {
                echo "Sanity Test on Dev .."
            }
        }
    }
}
