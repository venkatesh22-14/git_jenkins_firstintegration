pipeline {
    agent any
    tools { 
      maven 'maven-3.6.3' 
    }

    stages {
        stage ('Compile Stage') {

            steps {
                //withMaven(maven : 'apache-maven-3.6.3') {
               // def mvnHome = tool name: 'mvn', type: 'maven' {
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
                    sh 'mvn deploy'
                //}
            }
        }
    }
}
