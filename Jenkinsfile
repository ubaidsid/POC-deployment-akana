pipeline {
    agent any
    stages {
        stage('deployment') {
            steps {
           wget --no-check-certificate --quiet \
  --method POST \
  --timeout=0 \
  --header 'Authorization: Basic dWJhaWQudXJyZWhtYW5AaW5mb3N5cy5jb206QEthc2h1MTEyMjMzNDQh' \
  --header 'Content-Type: application/json' \
  --body-data '{
  "email":"ubaid.urrehman@infosys.com",
  "password":"@Kashu11223344!",
  "federationLogins":true
}' \
   'https://preprod-portal-entapi.spectrummobile.com/api/login'
        }
        stage('Test cases') {
            steps {
                echo "Sanity Test on Dev .."
            }
        }
    }
}
