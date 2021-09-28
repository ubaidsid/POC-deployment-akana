pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        /* CORRECT */
        import groovyx.net.http.HTTPBuilder
import static groovyx.net.http.ContentType.*
import groovyx.net.http.ContentType
import static groovyx.net.http.Method.*

def project = 'app-ne-preprod-lls-atlassian'
def topic = 'xyz_project_all_issue_events'
def access_token = 'ya29.c.KmC6B7IHIUh8afwaYc5KNSwlEtiyTVXLvcRDjd-t6WJFESYPlV4kxmDB9vAhO9snExsPJVYzd2SXIl5uBQMVlDRwsCl1ORpdDD5Pt697tGdA5rxrYZpAR1Yhz6CC9FMAhbY'

def http = new HTTPBuilder("https://abc.googleapis.com/v1/projects/$project/topics/$topic:publish")

http.request(POST) {
   //uri.path = 'https://abc.googleapis.com/v1/projects/$project/topics/$topic:publish'
   requestContentType = ContentType.JSON
   headers.'Authorization' = "token $access_token"
   body = [messages: [data: "test"]]
   response.success = { resp ->
      println "Success! ${resp.status}"
   }
   response.failure = { resp ->
      println "Request failed with status ${resp.status}"
   }
}
      }
    }
  }
}
