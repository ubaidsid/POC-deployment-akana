pipeline {
    agent any
    stages {
        stage('deployment') {
            steps {
                result=$(curl -X POST -H 'Content-Type: application/json' -H 'Accept: application/json' -i -k 'https://preprod-portal-entapi.spectrummobile.com/api/login' --data '{
   "email":"ubaid.urrehman@infosys.com",
   "password":"@Kashu11223344!",
   "federationLogins":true
 }')
echo "Response from server"
echo $result
exit
            }
        }
        stage('Test cases') {
            steps {
                echo "Sanity Test on Dev .."
            }
        }
    }
}
