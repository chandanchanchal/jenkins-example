pipeline {
    agent { label 'slave1'}

    stages {
        stage ('Compile Stage') {

            steps {
                  sh 'cho $JOB_NAME'
                withMaven(maven : 'MAVEN_HOME') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MAVEN_HOME') {
                    sh 'mvn test'
                }
            }
        }



    }
}
