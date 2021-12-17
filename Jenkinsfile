pipeline {
    agent any
    environment {
        PATH = "/opt/apache-maven-3.6.3/bin:$PATH"
    }
    stages {
        stage ('Compile Stage') {

            steps {
                //withMaven(maven : 'apache-maven-3.6.3') {
               //def mvnHome = tool name: 'mvn', type: 'maven' {
                     sh 'mvn clean compile'
                //}
            }
        }

        stage ('Testing Stage') {

            steps {
                //withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn test'
                //}
            }
        }


        stage ('Deployment Stage') {
            steps {
                //withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn install'
                //}
            }
        }
        
       stage ('Email Notification) {
            
              steps {
                  post {
                        failure {
                              // The developer setting up this job can specify which group should receive an email when the build fails
                              mail to: "${srilakshmivenkatesh2214@gmail.com}",
                                subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
                                body: "Something is wrong with ${env.BUILD_URL}"
                        }
                  }
              }
              }
              }
              }
   
