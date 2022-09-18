pipeline {
    agent {label 'develop'}

    stages {
        stage ('Compile Stage') {

            steps {
                echo 'Hello from develop'
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
