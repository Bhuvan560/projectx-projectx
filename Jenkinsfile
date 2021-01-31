rabbitmq {
      def app
      stage('Clone repository') {

            checkout scm
      }
      stage('Build image') {

            app = docker.build("bhuvan06/projectx-rabbitmq")
       }
      stage('Push image') {
                      docker.withRegistry('https://registry.hub.docker.com', 'git') {
       app.push("${env.BUILD_NUMBER}")
       app.push("latest")
              }
           }
        }

